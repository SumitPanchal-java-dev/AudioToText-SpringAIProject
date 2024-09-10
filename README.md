# Audio Translator

A Spring Boot application for audio transcription using OpenAI's Whisper model. This project allows users to upload audio files and get their transcriptions in text format.

## Features

- Upload audio files in WAV format.
- Transcribe audio using OpenAI's Whisper model.
- Simple and user-friendly frontend for interacting with the API.

## Prerequisites

- Java 17 or later
- Maven or Gradle
- Spring Boot
- OpenAI API Key

## Setup


Configuration
Set up OpenAI API Key:

Create an OpenAI account and obtain an API key from OpenAI API.

Application Properties:

Update src/main/resources/application.properties with your configuration:
properties
Copy code
spring.application.name=audiotranslator
spring.ai.openai.api-key=${SPRING_AI_OPENAI_API_KEY}
spring.ai.openai.audio.speech.base-url=http://api.openai.com
spring.ai.openai.audio.transcription.options.model=whisper-1
spring.ai.openai.audio.transcription.options.response-format=json

Access the Application

Frontend: Open your browser and navigate to http://localhost:8080.
API Endpoint: POST /api/transcribe for transcribing audio files.

Frontend
The frontend is located in src/main/resources/static/index.html and includes:

File upload input
Button to trigger transcription
Result display area
