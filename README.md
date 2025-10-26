
1. Copy `.env.example` to `.env` and update the values as needed.
2. Run `docker-compose up` to start the services.
3. Access the service via `http://localhost:8080`.


To induce chaos on the active service:
- For Blue: `curl -X POST http://localhost:8081/chaos/start?mode=error`
- For Green: `curl -X POST http://localhost:8082/chaos/start?mode=error`

To stop chaos:
- For Blue: `curl -X POST http://localhost:8081/chaos/stop`
- For Green: `curl -X POST http://localhost:8082/chaos/stop`
