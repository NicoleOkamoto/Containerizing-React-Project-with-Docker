# Praticing setting up React Project in a Docker Container

This project sets up a development environment for a Create React App application, displaying a `<h1>` tag with the text "Codin 1". The application is hosted in a Docker container.

## Requirements

- Docker

## Instructions

Follow these steps to get the web application running on `localhost:7775` (127.0.0.1:7775):

### Step 1: Clone the Repository

If you haven't already, clone the repository containing the project files:

```bash
git clone <repository_url>
cd <repository_directory>
```

To find the repository_url On GitHub: 
1. Click on the green "Code" button.
2. Copy the HTTPS or SSH URL from the dropdown.
3. Replace on the ```bash

### Step 2: Build the Docker Image

Build the Docker image using the provided `Dockerfile`. Run this command from the root of your project directory (where the Dockerfile is located):

```bash
docker build -t okamoto_nicole_coding_assignment11 .
```

### Step 3: Run the Docker Container

Run the Docker container using the following command:

```bash
docker run -it --rm -p 7775:3000 --name okamoto_nicole_coding_assignment11 okamoto_nicole_coding_assignment11
```

### Step 4: Access the Web Application

Open your web browser and navigate to `http://localhost:7775`. You should see the web application displaying a `<h1>` tag with the text "Codin 1".

## Notes

- The container maps port 3000 (default for Create React App) to port 7775 on your localhost, therefore on your browser navigatete to: `http://localhost:7775` 
- The `--rm` flag ensures that the container is removed after you stop it.
- The `-it` flag allows you to interact with the container (useful for debugging).

## Troubleshooting

- If the container fails to start, ensure you have Docker installed and running on your machine.
- Check for any errors in the terminal output and address them accordingly.
```
