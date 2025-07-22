# Self Stack Docker

Self Stack Docker is a containerized solution for easy deployment of self-hosted applications with secure configurations.

## Prerequisites

- Docker and Docker Compose installed on your system.
- Required environment variables set (see below).

## Setup Certificate

To generate SSL certificates for secure connections, follow these steps:

```bash
cp certificate/ssl.conf.template certificate/ssl.conf
bash certificate/generate.sh
```

## Setup Environment Variables

Prepare your environment variables by copying and editing the template:

```bash
cp .env.template .env
```

### Required Environment Variables

Make sure to define the following variables in your `.env` file:

1. `SELF_STACK_TUNNEL_TOKEN` - Token for secure tunneling using Cloudflare Tunnel.
    - https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/
2. `SELF_STACK_POSTGRESQL_PASSWORD` - Password for the PostgreSQL database.

## Running the Stack

Start all services in detached mode with Docker Compose:

```bash
docker compose up -d
```

## Additional Information

- For advanced configuration, you can edit the files in the `certificate` directory and the `.env` file according to your needs.
- Logs and runtime data will be managed by Docker.

## License

This project is licensed under the MIT License.