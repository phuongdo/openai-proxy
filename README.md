# Docker Nginx OpenAI API Reverse proxy

This project is a simple Docker Nginx project that serves as a OpenAI API as a proxy
Nginx here is preconfigured to work on OpenAI API.

### Features:

- **Works with any client** that allows you to configure the server address (as it acts as a reverse proxy)


## Getting Started

### Prerequisites

- Docker
- Docker compose

### Installation

1. Clone the repository:

```
git clone https://github.com/phuongdo/openai-proxy.git
cd openai-pr
```

3. Start the container:

```
docker-compose up -d
```

4. Follow the logs

```
docker-compose logs -f
```

5. Stop the container:

```
docker-compose down
```

### Usage

Set your client's API server address to `http://localhost:9090`

```
curl http://localhost:9090/v1/chat/completions \
-H "Content-Type: application/json" \
-d '{
"model": "gpt-3.5-turbo",
"messages": [{"role": "user", "content": "Say this is a test!"}],
"temperature": 0.7
}'
```

### Configuration

The cache is configured using the `nginx.conf`. You can modify this file to change the cache settings or add additional URIs.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue if you encounter any problems or have suggestions for improvements.
