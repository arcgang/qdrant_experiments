
Running qdrant locally with podman 
<hr />

### Running Qdrant on mac using podman
export CONTAINERS_MACHINE_PROVIDER=applehv
podman machine init --rootful
podman machine start
podman run -p 6333:6333 -p 6334:6334 --privileged -v $PWD/qdrant_storage:/qdrant/storage qdrant/qdrant