# Award Generator

An AI-powered award citation generator designed to streamline the creation of professional military and civilian award nominations for the Defense Health Agency (DHA). Part of the SEMOSS PMO Portal suite.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Documentation](#documentation)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Overview

The Award Generator automates the creation of professional award citations and nominations using AI-powered analysis. It provides an intuitive interface for candidate information input, document upload, AI-generated citation creation, iterative refinement, and draft management.

Built as part of the SEMOSS PMO Portal, this application leverages advanced language models to deliver context-aware, high-quality award citations tailored to specific award types. The system reduces manual effort, ensures consistent formatting, and enhances the quality of award nominations across the organization.

---

## Key Features

- **Multiple Award Types**: Support for various DHA military and civilian awards with pre-configured citation templates
- **Document Upload**: Upload supporting documents (PDF, DOCX, PPT, TXT) to provide context for award generation
- **AI-Powered Generation**: Utilizes Large Language Models (LLMs) to create professional award citations
- **Flexible Input**: Enter candidate information manually or upload supporting documents
- **Version Control**: Track multiple versions of generated citations with comparison capabilities
- **Iterative Refinement**: Provide feedback to improve generated content through multiple iterations
- **Draft Management**: Save and manage multiple drafts with persistent storage
- **Copy to Clipboard**: Quick copy functionality for generated citations
- **Database Integration**: Store and retrieve drafts and award templates from SEMOSS database
- **Markdown Rendering**: View generated citations with rich text formatting

---

## Technology Stack

### Frontend
- **React 17** - UI framework
- **TypeScript** - Type-safe JavaScript
- **Material UI v5** - Component library with modern design
- **MobX** (v6.13.7) - State management with persistence support
- **React Router v6** - Client-side routing
- **Styled Components** (v5.3.11) - Component styling
- **React Markdown** (v8.0.7) - Markdown rendering
- **React Dropzone** (v14.2.3) - File upload functionality
- **Webpack 5** - Module bundler

### Backend
- **Java 8** - Backend processing
- **Maven** - Build and dependency management
- **Apache POI** - Document parsing (DOCX, PPT)
- **PDFBox** - PDF text extraction
- **SEMOSS Reactors** - Custom backend processing logic

### AI Integration
- **SEMOSS SDK** (v1.0.0-beta.14) - Core AI functionality
- **SEMOSS SDK React** (v1.0.0-beta.15) - React integration

---

## Installation

### Frontend Setup
```bash
# Navigate to client directory
cd assets/client

# Install dependencies using pnpm
pnpm install
```

### Backend Setup
```bash
# Navigate to backend directory
cd assets/awards-generator-be

# Clean and install Maven dependencies
mvn clean install
```

---

## Configuration

### Environment Variables
Create a `.env` file in the `assets/client` directory:
```env
# SEMOSS Configuration
MODULE=your-module-name
ACCESS_KEY=your-access-key
SECRET_KEY=your-secret-key
APP=your-app-id
DATABASE=your-database-id

# Optional: Development settings
NODE_ENV=development
PORT=3000
```

---

## Usage

### Starting Development Server
```bash
# In assets/client directory
pnpm install
pnpm dev

# Application will be available at http://localhost:3000
```

### Workflow

1. **Select Award Type and AI Model** - Navigate to `/awards/new` and choose from available DHA award types and LLM models
2. **Provide Candidate Information** - Enter information manually, upload documents (PDF, DOCX, PPT, TXT), or combine both
3. **Generate Citation** - Click "Generate" to create the award citation with markdown rendering
4. **Refine with Feedback** - Provide feedback and regenerate to improve the citation
5. **Manage Versions** - Compare different iterations and select the best version
6. **Save and Access Drafts** - Drafts are automatically saved and accessible from the sidebar
7. **Copy Citation** - Use "Copy to Clipboard" to paste into award nomination forms

### Building for Production
```bash
# Build frontend
cd assets/client
pnpm build

# Build backend
cd assets/awards-generator-be
mvn clean package

# Output: target/awards-generator-be-0.0.1-SNAPSHOT.jar
```

---

## Deployment

### Build the Application
```bash
# Build frontend
cd assets/client
pnpm build

# Build backend
cd assets/awards-generator-be
mvn clean package
```

### Upload to Govconnect.ai
- Compress the `portals/` directory to a zip file
- Create a new app and upload the zip file to version/assets/
- Configure environment variables and publish the portal

---

## Contributing

We welcome contributions to improve the Award Generator! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on:
- Reporting bugs and suggesting enhancements
- Development workflow and setup
- Testing your changes
- Documentation guidelines
- Release process

---

## Documentation
- **Comprehensive Documentation**: See `_PMO_Documentation.pptx` for detailed information
- **SEMOSS SDK Documentation**: [https://semoss.org/docs](https://semoss.org/docs)
- **Material UI Documentation**: [https://mui.com](https://mui.com)
- **React Documentation**: [https://react.dev](https://react.dev)
- **TypeScript Documentation**: [https://www.typescriptlang.org/docs](https://www.typescriptlang.org/docs)
- **MobX Documentation**: [https://mobx.js.org](https://mobx.js.org)

---

## License

This project is proprietary software developed for the Defense Health Agency (DHA). All rights reserved.

**Authorized Use Only**: This software is for official use by authorized DHA personnel and contractors only. Unauthorized access, use, or distribution is strictly prohibited.

---

## Acknowledgments

This project is built using the following key technologies:

- **[React](https://react.dev)** - UI framework
- **[Material UI](https://mui.com)** - Component library
- **[SEMOSS](https://semoss.org)** - AI and analytics platform
- **[TypeScript](https://www.typescriptlang.org)** - Type-safe JavaScript
- **[Apache POI](https://poi.apache.org)** - Document processing

---
