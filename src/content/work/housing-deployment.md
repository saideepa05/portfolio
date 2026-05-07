---
title: End-to-End ML Deployment Pipeline
publishDate: 2026-01-01 00:00:00
img: /assets/work/housing-deployment.jpg
img_alt: Machine learning deployment pipeline for California housing price prediction
description: |
  A fully automated ML deployment pipeline predicting California housing prices —
  Flask web app, Docker containerization, and GitHub Actions CI/CD pushing to
  Heroku on every commit with zero manual intervention.
tags:
  - MLOps
  - Flask
  - Docker
  - CI/CD
  - Python
---

## Overview

Engineered a production-grade machine learning deployment pipeline predicting California housing prices using linear regression, complete with automated CI/CD infrastructure. Built a professional Flask web interface with a custom dark-themed design, containerized the application with Docker for environment portability, and wired up GitHub Actions to automatically build, containerize, and deploy to Heroku on every push to main — zero manual steps required.

**GitHub:** [saideepa05/housing_deployment](https://github.com/saideepa05/housing_deployment)

## What I Built

- **Flask web application** — responsive dark-themed UI with a `/predict` REST endpoint, strict numeric input validation, and explicit feature mapping to the trained model
- **Linear regression model** — retrained with scikit-learn to resolve version compatibility issues that would break inference in production
- **Docker containerization** — full Dockerfile packaging the app, model, and dependencies for consistent behaviour across development and production environments
- **GitHub Actions CI/CD pipeline** — automated workflow triggered on push to main: builds the container, authenticates with Heroku CLI, and deploys with zero-downtime releases
- **Infrastructure debugging** — resolved scikit-learn version mismatches and Heroku CLI ENOENT spawn errors that blocked the initial pipeline, resulting in a fully reliable deploy chain

## Tech Stack

Python · Flask · scikit-learn · Pandas · NumPy · Docker · GitHub Actions · Heroku · HTML/CSS

## Results

Delivered a fully automated deployment pipeline with zero manual intervention — a push to main triggers containerization and production release end-to-end. Resolved critical infrastructure blockers at every layer (model versioning, container builds, Heroku CLI integration) and implemented robust input validation, resulting in a production-ready application serving real-time housing price predictions.
