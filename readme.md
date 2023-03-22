# do this
## create images
cd lost_island_frontend
podman build -t skull/lost_island_frontend .

cd ..
cd lost_island_backend
podman build --build-arg JAR_FILE=build/libs/*.jar -t skull/lost_island_backend .

## Deploy on Kubernetes
run lost_island_deployment.yaml


