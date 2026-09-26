# Technical Documentation: MinIO Deployment

## Deployment Command

The MinIO S3-compatible object storage server was deployed using Docker with the following command:

```bash
docker run -d \
  -p 9000:9000 \
  -p 9001:9001 \
  --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  minio/minio server /data --console-address ":9001"
```

## Command Explanation

| Command | Description |
|---|---|
| `docker run -d` | Runs the MinIO container in detached mode. |
| `-p 9000:9000` | Maps port `9000` for the MinIO API. |
| `-p 9001:9001` | Maps port `9001` for the MinIO web console. |
| `--name minio-server` | Assigns the container the name `minio-server`. |
| `-e "MINIO_ROOT_USER=cloudadmin"` | Sets the MinIO administrator username. |
| `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` | Sets the MinIO administrator password. |
| `minio/minio` | Specifies the MinIO Docker image. |
| `server /data` | Starts MinIO using `/data` as the storage directory. |
| `--console-address ":9001"` | Configures the MinIO web console to run on port `9001`. |

## Port Configuration

The deployment uses two ports:

- **Port 9000** – MinIO S3 API
- **Port 9001** – MinIO Web Console

The web console can be accessed through the cloud playground's forwarded port for `9001`.

## Container Verification

After deployment, the running container can be verified using:

```bash
docker ps
```

The `minio-server` container should appear in the list of running containers.

To view the container logs, use:

```bash
docker logs minio-server
```

These commands help confirm that the MinIO server started successfully and is ready to accept connections.
