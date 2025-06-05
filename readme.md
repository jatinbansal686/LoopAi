# Data Ingestion API System

## Overview

This project implements a RESTful API system for ingesting data requests asynchronously with priority handling and rate limiting.  
It simulates fetching and processing data batches with controlled concurrency and priority queuing.

---

## Features

- **POST /ingest**: Submit a list of IDs with priority (HIGH, MEDIUM, LOW) for ingestion.
- **GET /status/:ingestion_id**: Check the status of the ingestion request and batches.
- Processes IDs in batches of 3 asynchronously.
- Rate limits batch processing to 1 batch every 5 seconds.
- Higher priority requests are processed before lower priority ones.
- Input validation and user-friendly error messages.
- Status tracking for ingestion and batches.

---

## Tech Stack

- Node.js with Express.js
- MongoDB (can be configured to use MongoDB Atlas)
- Mongoose for ODM
- Async queue for batch processing
- UUID for unique ingestion and batch IDs

---

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
