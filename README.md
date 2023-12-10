# detector-insightface-docker

```sh
docker-compose build
docker-compose up -d

curl -X POST \
  --header "Content-Type: multipart/form-data" \
  --form "file=@pakutaso_43730.jpg;type=image/jpeg" \
  http://localhost:8000/detect

curl -X POST \
  --header "Content-Type: multipart/form-data" \
  --form "file=@pakutaso_43730.npy;type=application/octet-stream" \
  http://localhost:8000/detect

curl -X POST \
  --header "Content-Type: application/json" \
  --data-binary @embeddings.json \
  http://localhost:8000/compare

open http://localhost:8001/
```