# Song API

Backend for the Song App built with Spring Boot, JPA, and H2.

## Local development

Run the API:

```bash
./mvnw spring-boot:run
```

The app starts on `http://localhost:8080` and exposes:

- `GET /lumba/songs`
- `GET /lumba/songs/{id}`
- `GET /lumba/songs/search/{keyword}`
- `POST /lumba/songs`
- `PUT /lumba/songs/{id}`
- `DELETE /lumba/songs/{id}`

The API seeds starter song data automatically on boot so the frontend has content immediately.

## Render deployment

Create a Web Service on Render from this repository.

- Runtime: `Docker`
- Dockerfile: `./Dockerfile`
- Health Check Path: `/lumba/songs`

Optional environment variable:

```env
FRONTEND_ORIGIN=https://<your-song-ui>.onrender.com
```

If you leave `FRONTEND_ORIGIN` unset, the API keeps CORS open so the school project can connect easily.

The repository also includes `render.yaml` for Blueprint-based setup.
