# Estratégias de Cache

- Cache é uma técnica de armazenamento temporário de dados frequentemente acessados para reduzir a latência e melhorar o desempenho do aplicativo
- No NestJS, o sistema de cache permite armazenar resultados de consultas ou operações custosas em memória para acesso rápido

```bash
npm install @nestjs/cache-manager cache-manager
```

- O NestJs possui um módulo de cache extensível que pode ser implementado nas nossas aplicações

- Os métodos do módulo de cache são abstraídos, portanto podemos utilizar algumas stores para o nosso sistema de cache, como:
    - In-memory
    - Redis
    - Mongo
    - E vários outros sistemas distribuídos


```ts
import { Module } from '@nestjs/common';
import { CacheModule } from '@nestjs/cache-manager';
import { AppController } from './app.controller';

@Module({
    imports: [CacheModule.register({ isGlobal: true })],
    controllers: [AppController],
})
export class AppModule {}
```

- O Cache pode ser definido de forma por controller ou por endpoint via decorators de forma automática

```ts
@Get()
@UseInterceptors(CacheInterceptor)
@CacheTTL(30000)
async findAll() {
    return this.projectsService.findAll();
}
```

- Podemos também utilizar o cache manager service para customizarmos a forma como armazenamos o cache por meio de uma lógica específica

```ts
@Controller("projects")
export class ProjectsController {
    constructor(
        private readonly projectsService: ProjectsService,
        @Inject(CACHE_MANAGER) private cacheManager: Cache,
    ) {}

    @Get()
    async findAll(@Query() filter?: FilterDto) {
        const projectsCache = this.cacheManager.get("projects");
        if (projectsCache) {
            return projectsCache;
        }
        const results = await this.projectsService.findAllPaginated(filter);
        this.cacheManager.set("projects", results);
        return results;
    }
}
```

## Redis

- Para implementação do cache via redis, podemos utilizar as opções da instância do CacheModule e passar as referências para o host onde o redis encontra-se hospedado

```ts
CacheModule.register({
    isGlobal: true, 
    store: redisStore,
    host: process.env.REDIS_HOST,
    port: process.env.REDIS_PORT
})
```