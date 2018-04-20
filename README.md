
### Docker

```bash
$ docker run -d -p 9411:9411 openzipkin/zipkin
```

### Architecture

```text
 :: Sleuth with Zepkin ::
        
                  docker(zipkin)
 ┌──────────────────┐
 │ a-service (8081) │
 └──────────────────┘
        │         ┌──────────────────┐
        └───────> │ b-service (8082) │
                  └──────────────────┘
                       │         ┌─────────────────┐
                       └───────> │ c-service(8083) │
                                 └─────────────────┘
```