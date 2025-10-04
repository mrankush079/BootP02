1) The Application class with @SpringBootApplication is the entry point: when you run it, Spring Boot starts up, scans for components, and configures everything automatically.
2) The Repository (e.g. StudentRepo) is the data layer; it “fetches” data (in your toy example, returns a hard coded string).
3) The Service layer holds business logic: the controller asks it for data, it asks the repository, maybe does processing, and returns results.
4) The Controller (annotated @RestController) handles HTTP requests (e.g. GET /welcome), calls the service, and returns its result directly as the HTTP response.
