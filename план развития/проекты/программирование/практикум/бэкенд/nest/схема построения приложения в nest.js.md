
все построено на модулях
есть корневой модуль 

```
import { Module } from '@nestjs/common';
import { UsersModule } from './users/users.module';
import { PostsModule } from './posts/posts.module';
import { ConfigModule } from './config/config.module'

@Module({
  imports: [UsersModule, PostsModule, ConfigModule],
  controllers: [],
  providers: [],
})
export class AppModule {}
```
есть дочерние модули

```
import { Module } from '@nestjs/common';
import { UsersService } from './users.service';
import { UsersController } from './users.controller';

@Module({
  controllers: [UsersController],
  providers: [UsersService],
})
export class UsersModule {}
```
бизнес-логика в UsersService
ручки в контроллерах
