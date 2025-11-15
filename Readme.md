
# Traffic Congestion Detection Application

## Overview

This is a Traffic congestion detection application built with FastAPI, leveraging machine learning models to analyze and predict traffic conditions from video inputs. Developed as a group project under the Center of Excellence in AI & ML, it provides a robust API for processing both video and individual frame predictions.

## Features

- Upload video files to predict traffic conditions.
- Upload images to predict traffic conditions from single frames.
- Health check endpoint to verify the status of the application.
- API endpoints to retrieve model information and available traffic classes.

## Tech Stack
- **Backend Framework:** FastAPI
- **Machine Learning Library:** Keras (with TensorFlow backend)
- **Image Processing:** OpenCV
- **Containerization:** Docker
- **Environment Management:** Python 3.9
- **Logging:** Custom logging configuration
- **CI/CD:** GitHub Actions for automated deployment to AWS EC2.

## Getting Started

### Prerequisites

- Docker installed on your machine.
- Python 3.9 (if you wish to run locally outside Docker).

### Clone the Repository

```bash
git clone https://github.com/Sankeerthan13/Traffic-Congestion-Detection.git
cd Traffic-Congestion-Detection
```

### Build the Docker Image

```bash
docker build -t traffic-prediction-app .
```

### Run the Docker Container

```bash
docker run -d -p 8000:8000 --name traffic-prediction-api traffic-prediction-app
```

### Access the Application

The application will be accessible at `http://localhost:8000`.

### API Endpoints

- `GET /`: Home page (HTML response).
- `GET /health/`: Check application health.
- `GET /model-info/`: Get information about the model.
- `GET /traffic-classes/`: Retrieve available traffic classes.
- `POST /predict-video/`: Upload a video file to get predictions.
- `POST /predict-image/`: Upload a single image to get predictions.

## Logging

Logs are configured for both server activity and model processing, enabling easy debugging and monitoring.
