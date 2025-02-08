
# Podcast Generator

## Overview

The **Podcast Generator** project is a simple solution for generating podcast RSS feeds. This repository provides the necessary components to create, customize, and publish podcast feeds. It leverages Docker for containerization and a Python script (`feed.py`) to handle the RSS generation. This tool can be adapted for various podcasting needs.

## Files in the Repository

1. **`Dockerfile`**: Defines the Docker image used to containerize the podcast generation process.
2. **`entrypoint.sh`**: A shell script that initializes the process when the Docker container starts.
3. **`feed.py`**: A Python script that generates the RSS feed for the podcast.
4. **`action.yml`**: Defines a GitHub Action that could be used for automating the process of generating and updating the podcast feed.
5. **`LICENSE`**: The MIT license governing the usage of this project.
6. **`README.md`**: This file, providing an overview and instructions for using the repository.

## Getting Started

### Prerequisites

Ensure that you have Docker installed on your machine. You can follow [Docker's official installation guide](https://docs.docker.com/get-docker/) for setup instructions.

### Building the Docker Image

To build the Docker image for this project, run the following command:

```bash
docker build -t podcast-generator .
```

This will create a Docker image named `podcast-generator`.

### Running the Application

Once the image is built, you can run it as a container:

```bash
docker run -v /path/to/your/audio/files:/audio podcast-generator
```

This will execute the podcast generation process. Ensure that your audio files are placed in the specified directory (`/audio`) and accessible from the container.

## Usage

1. **Generate RSS Feed**: The `feed.py` script generates an RSS feed file that can be used for your podcast distribution.
2. **Customize the Feed**: You may need to modify the Python script (`feed.py`) to fit your specific podcast's metadata and episodes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
