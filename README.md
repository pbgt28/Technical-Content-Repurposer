# Autonomous Technical Content Repurposer & Social Multi-Poster

An AI-powered content automation workflow built using **n8n, OpenAI, Jina Reader, APIs, and Google Sheets**. The project transforms technical blogs and whitepapers into platform-ready social media content, including LinkedIn carousel scripts and Twitter/X threads.

## Overview

Technical articles and whitepapers often contain valuable insights that require considerable effort to adapt for social media. This project automates the content repurposing process by extracting source material, generating platform-specific content using an AI agent, structuring the outputs, and storing them in Google Sheets.

The workflow is triggered through an API request, allowing a technical article or whitepaper URL to be submitted for processing.

## Key Features

- **API-Based Triggering:** Accepts content URLs through a webhook, with requests testable using Postman.
- **Automated Content Extraction:** Uses Jina Reader to retrieve readable content from source URLs.
- **AI-Powered Repurposing:** Uses an OpenAI-powered agent to transform technical material into social media content.
- **LinkedIn Carousel Scripts:** Generates structured content suitable for LinkedIn carousel posts.
- **Twitter/X Threads:** Produces five-post social media threads from technical source material.
- **Structured Output Parsing:** Organizes generated content into a consistent format.
- **Google Sheets Integration:** Stores the generated content for review, tracking, and further use.

## Workflow Architecture

The workflow follows this sequence:

1. **Webhook Trigger:** Receives a content URL through an API request.
2. **Content Extraction:** Retrieves readable text from the submitted technical article or whitepaper using Jina Reader.
3. **Repurpose Content Agent:** Uses an OpenAI model to analyze the source and generate platform-specific content.
4. **Content Structure Parser:** Formats the generated content into a structured output.
5. **Google Sheets Storage:** Saves the resulting carousel scripts and social media threads.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation and orchestration |
| OpenAI | AI-powered content generation |
| Jina Reader | Web content extraction |
| Webhooks | API-based workflow triggering |
| Postman | Testing API requests |
| Google Sheets | Content storage and organization |
| Structured Output Parser | Consistent output formatting |

## How It Works

1. Submit a technical blog or whitepaper URL through a Postman request.
2. The webhook receives the URL and triggers the workflow.
3. Jina Reader extracts readable content from the source.
4. The OpenAI-powered agent analyzes the extracted material and generates platform-specific content.
5. The structured output parser organizes the generated content.
6. The results are stored in Google Sheets for review and future use.

## Generated Content

The workflow is designed to generate two types of content:

### 1. LinkedIn Carousel Scripts

Transforms technical concepts into structured, slide-by-slide content suitable for professional audiences.

### 2. Twitter/X Threads

Converts technical material into a five-post thread designed to communicate key concepts in a concise, connected format.

## Implementation and Testing

The workflow was tested with technical sources covering topics such as:

- Operating Systems
- Thermodynamics
- Data Science
- Machine Learning
- SQL

The tested workflow produced LinkedIn carousel scripts and five-post social media threads for the submitted sources, with outputs organized in Google Sheets.

## Setup and Configuration

### Prerequisites

- An n8n instance (cloud or self-hosted)
- An OpenAI API key
- Access to Jina Reader
- A Google account with Google Sheets access
- Postman for API testing

### Configuration Steps

1. Import or recreate the workflow in n8n.
2. Configure the webhook to accept a content URL.
3. Set up the content extraction step using Jina Reader.
4. Configure OpenAI credentials and the content repurposing agent.
5. Define the expected structure for carousel scripts and social media threads.
6. Configure Google Sheets credentials and map the output fields to the appropriate columns.
7. Test the webhook by sending a sample URL through Postman.
8. Verify the generated content and its storage in Google Sheets.

**Security:** Keep API keys and credentials in n8n's credential manager. Do not commit secrets or private webhook URLs to a public repository.

## Use Cases

- Repurposing technical blogs into social media content
- Converting whitepapers into accessible educational posts
- Creating LinkedIn carousel drafts
- Generating Twitter/X educational threads
- Organizing content for a social media calendar
- Automating repetitive content preparation tasks

## Future Improvements

- Add direct publishing integrations for supported social platforms.
- Introduce human review and approval before publication.
- Add duplicate-content checks.
- Support additional content formats and social media platforms.
- Track publication status and engagement metrics.

## Project Status

Developed and tested as an AI-powered content repurposing and workflow automation project using n8n.
