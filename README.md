# Node.js Demo App

A simple Node.js application demonstrating a CI/CD pipeline using GitHub Actions and Docker.

## Technologies Used

* Node.js
* Docker
* DockerHub
* GitHub
* GitHub Actions

## Project Structure

```text
nodejs-demo-app/
├── app.js
├── Dockerfile
├── package.json
├── README.md
└── .github/
    └── workflows/
        └── main.yml
```

## CI/CD Pipeline

The project uses GitHub Actions to automate the Docker image build and deployment process.

### Workflow

1. Code is pushed to the GitHub repository.
2. GitHub Actions automatically starts the workflow.
3. The Node.js application is built and tested.
4. A Docker image is created.
5. GitHub Actions logs in to DockerHub using GitHub Secrets.
6. The Docker image is pushed to DockerHub.
7. The workflow completes successfully.

## GitHub Secrets

The following GitHub repository secrets are used:

* `DOCKERHUB_USERNAME`
* `DOCKERHUB_TOKEN`

The DockerHub token is stored securely as a GitHub Secret and is not included in the source code.

## Run the Application Locally

Install the dependencies:

```bash
npm install
```

Run the application:

```bash
node app.js
```

## Build Docker Image

```bash
docker build -t nodejs-demo-app .
```

## Run Docker Container

```bash
docker run -p 3000:3000 nodejs-demo-app
```

The application can then be accessed locally on port `3000`.

## GitHub Actions

The CI/CD workflow is located at:

```text
.github/workflows/main.yml
```

Every push to the repository can trigger the automated workflow.

## DockerHub

The Docker image is published to the project's DockerHub repository through GitHub Actions.

## Result

The GitHub Actions workflow completed successfully, confirming that the CI/CD pipeline is working.

## Author

Harshini
