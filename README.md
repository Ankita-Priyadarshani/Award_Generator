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

### Python Dependencies (for AI models)
```bash
pip install Dataset
pip install text_generation
```

### SEMOSS Configuration
Add to your SEMOSS instance's `RDF_Map.prop` file:
```properties
# Moose Model Configuration
MOOSE_MODEL guanaco
MOOSE_ENDPOINT https://play.semoss.org/moose
GUANACO_ENDPOINT https://play.semoss.org/moose/guanaco/
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

1. **Select Award Type**
   - Navigate to `/awards/new`
   - Choose from available DHA award types
   - Award templates are pre-configured with appropriate citation formats

2. **Select AI Model**
   - Choose your preferred LLM model from available options
   - Models are filtered for text-generation capabilities

3. **Provide Candidate Information**
   - **Option A**: Enter candidate information and accomplishments manually in the text area
   - **Option B**: Upload supporting documents (PDF, DOCX, PPT, TXT)
   - **Option C**: Combine both manual input and document uploads

4. **Generate Citation**
   - Click "Generate" to create the award citation
   - View generated content in real-time with markdown rendering
   - Draft is automatically saved to the database

5. **Refine with Feedback**
   - Review the generated citation
   - Provide specific feedback on what to improve
   - Click "Regenerate" to create an improved version
   - All versions are saved and accessible

6. **Version Navigation**
   - Use version navigation to compare different iterations
   - View feedback provided for each version
   - Select the best version for your needs

7. **Save and Manage Drafts**
   - Drafts are automatically saved to the database
   - Access previous drafts from the sidebar
   - Each draft maintains its full version history
   - Drafts persist across sessions and devices

8. **Copy Citation**
   - Use the "Copy to Clipboard" button to copy the citation
   - Paste into award nomination forms or documents

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
- Create a new app on Govconnect.ai portal
- Upload the zip file to version/assets/ (check "Unzip?" box)
- Configure environment variables (MODULE, ACCESS_KEY, SECRET_KEY, APP, DATABASE)
- Publish the portal from Settings → Data Apps tab

---

## Contributing

We welcome contributions to improve the Award Generator! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on:
- Code of conduct
- Development workflow
- Coding standards
- Pull request process
- Testing requirements
- Documentation guidelines

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

This project is built using the following technologies:

- **[React](https://react.dev)** - UI framework
- **[Material UI](https://mui.com)** - Component library
- **[MobX](https://mobx.js.org)** - State management
- **[SEMOSS](https://semoss.org)** - AI and analytics platform
- **[TypeScript](https://www.typescriptlang.org)** - Type-safe JavaScript
- **[Apache POI](https://poi.apache.org)** - Document processing
- **[PDFBox](https://pdfbox.apache.org)** - PDF text extraction
- **[Webpack](https://webpack.js.org)** - Module bundler
- **[pnpm](https://pnpm.io)** - Fast, disk space efficient package manager

---

