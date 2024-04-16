# NGINX Reverse Proxy Configuration

This repository contains a comprehensive NGINX configuration template designed to serve as a reverse proxy for web applications. It is structured to efficiently distribute incoming requests to backend servers, ensuring high availability and security for your applications.

## Key Features

- **Load Balancing**: Distributes incoming requests across multiple backend servers to optimize resource utilization and improve response times.
- **Failover Support**: Automatically redirects traffic to operational servers in case of server failure, ensuring uninterrupted service.
- **SSL/TLS Support**: Secures communication between clients and the server using SSL/TLS certificates.
- **Path-based Routing**: Directs requests to specific backend servers based on the request path, facilitating the management of different services within a single domain.

## Configuration Sections

### Upstream Server Definitions

Defines backend servers for the main application, API, and app paths in upstream.conf. This setup supports load balancing and failover. **Make sure to update your own upstream servers**

### HTTP and HTTPS Server Blocks

Includes configurations for both HTTP and HTTPS traffic. HTTP traffic is redirected to HTTPS for secure communication, and SSL/TLS certificates are configured for HTTPS.

### Reverse Proxy Configuration

Configures reverse proxy settings for the main path, API path, and app path, ensuring that requests to these paths are forwarded to the appropriate backend servers. Please update it with your application paths.

### Additional Configuration

Provides space for additional NGINX configuration directives, such as enabling Gzip compression, caching, and more.

## Getting Started

1. **Clone the Repository**: Use `git clone` to clone this repository to your local machine.
2. **Review and Customize**: Modify the upstream server definitions and paths as necessary to fit your specific deployment requirements.
3. **Deploy**: Apply the configuration to your NGINX server.