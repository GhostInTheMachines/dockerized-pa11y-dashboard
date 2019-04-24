# Dockerized pa11y-dashboard

## Setup Steps
- 1. Create Digital Ocean Droplet Docker on Ubuntu 18
- 2. SSH into server as root and create SSH keys on server
- 3. Copy and add key to Github
- 4. Clone this repo in the root home directory
- 5. Follow instructions below then point sub-directory to ip

A Docker container that runs [pa11y-dashboard](https://github.com/pa11y/dashboard).

Install from Docker Hub:

    docker pull squareweave/pa11y-dashboard

Build and run with `docker-compose`:

    docker-compose build
    docker-compose up
    
Or run on the hosting platform of your choice :)

## Environment Variables

**WEBSERVICE_DATABASE** (required) *no default*

Location of MongoDB, e.g. `mongodb://database/pa11y`.

**PORT** *default=80*

Port for the web server.

**WEBSERVICE_CRON** *default="0 30 0 \* \* \*"*

How often to run the web service.

Other environment variables are documented in [pa11y-dashboard](https://github.com/pa11y/dashboard).