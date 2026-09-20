# gerenciador-sala-reuniao

API Spring para reservar salas de reunião (nome, data, horário).

## Status

Estudo. Não está em produção.

## Para que serve

Backend do par fullstack com [client-room](https://github.com/mateusaledev/client-room). CRUD de salas em memória (H2), CORS liberado para `http://localhost:4200`.

## Stack

- Java 8 · Spring Boot 2.6 · Spring Data JPA · H2 · Bean Validation

## Como executar

Pré-requisitos: Java 8+, Maven.

```bash
git clone https://github.com/mateusaledev/gerenciador-sala-reuniao.git
cd gerenciador-sala-reuniao
./mvnw spring-boot:run
```

API em `http://localhost:8080`. O front Angular espera a porta **8082** — se for usar os dois juntos, mude `server.port` aqui ou o `baseUrl` no client.

## O que faz

```http
GET    /api/v1/rooms
GET    /api/v1/rooms/{id}
POST   /api/v1/rooms
PUT    /api/v1/rooms/{id}
DELETE /api/v1/rooms/{id}
```

Campos: nome, data, hora de início e fim.

## Estrutura

```
src/main/java/.../controller   RoomController
src/main/java/.../model        Room
src/main/java/.../repository   RoomRepository
```

## Front

https://github.com/mateusaledev/client-room
