# Contributing to Award Generator

First off, thank you for considering contributing to the Award Generator! It's people like you that make this application a great tool for the Defense Health Agency.

Following these guidelines helps to communicate that you respect the time of the developers managing and developing this open source project. In return, they should reciprocate that respect in addressing your issue, assessing changes, and helping you finalize your pull requests.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [What We're Looking For](#what-were-looking-for)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Your First Code Contribution](#your-first-code-contribution)
  - [Pull Requests](#pull-requests)
- [Style Guides](#style-guides)
  - [Git Commit Messages](#git-commit-messages)
  - [TypeScript Style Guide](#typescript-style-guide)
  - [Java Style Guide](#java-style-guide)
  - [Documentation Style Guide](#documentation-style-guide)
- [Development Setup](#development-setup)
- [Testing](#testing)
- [Community](#community)

---

## Code of Conduct

This project and everyone participating in it is governed by our commitment to maintaining a professional, respectful, and inclusive environment. By participating, you are expected to uphold this standard. Please report unacceptable behavior to the project maintainers.

### Our Standards

**Examples of behavior that contributes to a positive environment:**
- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

**Examples of unacceptable behavior:**
- The use of sexualized language or imagery and unwelcome sexual attention or advances
- Trolling, insulting/derogatory comments, and personal or political attacks
- Public or private harassment
- Publishing others' private information without explicit permission
- Other conduct which could reasonably be considered inappropriate in a professional setting

---

## What We're Looking For

There are many ways to contribute to the Award Generator, from writing tutorials or blog posts, improving the documentation, submitting bug reports and feature requests, or writing code which can be incorporated into the application itself.

**We particularly welcome contributions in the following areas:**
- Bug fixes and issue resolution
- New award type templates
- UI/UX improvements
- Performance optimizations
- Documentation enhancements
- Test coverage improvements
- Accessibility features
- Security enhancements

---

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v16+)
- pnpm (v10.11.1+)
- Java 8
- Maven 3+
- Git
- A text editor or IDE (VS Code recommended)

### Setting Up Your Development Environment

1. **Fork the repository** on your Git hosting platform
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/AwardGenerator.git
   cd AwardGenerator
   ```

3. **Create a branch** for your contribution:
   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Install frontend dependencies**:
   ```bash
   cd assets/client
   pnpm install
   ```

5. **Install backend dependencies**:
   ```bash
   cd ../awards-generator-be
   mvn clean install
   ```

6. **Configure environment variables**:
   - Copy `.env.example` to `.env` in `assets/client`
   - Fill in required values (contact maintainers for development credentials)

7. **Start the development server**:
   ```bash
   cd assets/client
   pnpm dev
   ```

---

## How to Contribute

### Reporting Bugs

**Before submitting a bug report:**
- Check the documentation to ensure it's not a configuration issue
- Search existing issues to avoid duplicates
- Update to the latest version to see if the issue persists

**When submitting a bug report, include:**
- A clear and descriptive title
- Detailed steps to reproduce the issue
- Expected behavior vs. actual behavior
- Screenshots or error messages (if applicable)
- Your environment details (OS, browser, Node.js version, etc.)
- Any relevant logs or stack traces

**Bug Report Template:**
```markdown
## Bug Description
A clear description of what the bug is.

## Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. Enter '...'
4. See error

## Expected Behavior
What you expected to happen.

## Actual Behavior
What actually happened.

## Environment
- OS: [e.g., Windows 10, macOS 12.0]
- Browser: [e.g., Chrome 96, Firefox 95]
- Node.js version: [e.g., 16.13.0]
- App version: [e.g., 0.0.1-SNAPSHOT]

## Additional Context
Any other context about the problem.
```

### Suggesting Enhancements

**Before submitting an enhancement:**
- Check if the enhancement has already been suggested
- Consider whether your idea fits the scope and aims of the project
- Provide detailed use cases and examples

**When suggesting an enhancement, include:**
- A clear and descriptive title
- A detailed description of the proposed functionality
- Explain why this enhancement would be useful
- List any alternative solutions or features you've considered
- Mockups, diagrams, or examples (if applicable)

### Your First Code Contribution

Unsure where to begin? Look for issues labeled:
- `good-first-issue` - Simple issues suitable for beginners
- `help-wanted` - Issues where we need community help
- `documentation` - Documentation improvements

### Pull Requests

**Before submitting a pull request:**
1. Ensure your code follows the project's style guides
2. Update documentation to reflect your changes
3. Add or update tests as needed
4. Run the linter and fix any issues: `pnpm lint:fix`
5. Ensure all tests pass
6. Update the README.md if adding new features

**Pull Request Process:**

1. **Create a descriptive PR title:**
   - `feat: Add new award type for civilian achievement`
   - `fix: Resolve draft save issue in Firefox`
   - `docs: Update installation instructions`
   - `refactor: Improve AwardForm component structure`

2. **Fill out the PR template** with:
   - Description of changes
   - Related issue number (if applicable)
   - Testing performed
   - Screenshots (for UI changes)
   - Checklist of completed tasks

3. **Link related issues** using keywords:
   - `Fixes #123`
   - `Closes #456`
   - `Related to #789`

4. **Request review** from maintainers

5. **Address feedback** promptly and professionally

6. **Keep your PR updated** with the main branch:
   ```bash
   git checkout main
   git pull upstream main
   git checkout your-feature-branch
   git rebase main
   ```

**Pull Request Template:**
```markdown
## Description
Brief description of what this PR does.

## Related Issue
Fixes #(issue number)

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## Testing
Describe the tests you ran and how to reproduce them:
- [ ] Test A
- [ ] Test B

## Checklist
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published

## Screenshots (if applicable)
Add screenshots to help explain your changes.
```

---

## Style Guides

### Git Commit Messages

Follow these conventions for clear, consistent commit messages:

**Format:**
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, semicolons, etc.)
- `refactor`: Code refactoring without changing functionality
- `test`: Adding or updating tests
- `chore`: Maintenance tasks, dependency updates

**Examples:**
```
feat(awards): Add support for Joint Service Commendation Medal

Implemented new award type with citation template and validation rules.
Added unit tests for award generation logic.

Closes #234
```

```
fix(drafts): Resolve version navigation crash in Safari

Fixed null pointer exception when navigating between draft versions
in Safari browser. Added proper null checks and error handling.

Fixes #456
```

**Guidelines:**
- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Capitalize the first letter
- No period at the end of the subject line
- Limit subject line to 50 characters
- Wrap body at 72 characters
- Separate subject from body with a blank line
- Use the body to explain what and why vs. how

### TypeScript Style Guide

**General Principles:**
- Use TypeScript for all new files
- Define types and interfaces explicitly
- Avoid `any` type when possible
- Use meaningful variable and function names
- Follow React functional component patterns

**Code Formatting:**
```typescript
// Use interfaces for object shapes
interface Award {
    id: string;
    name: string;
    prompt: string;
}

// Use function components with TypeScript
const AwardForm: React.FC<AwardFormProps> = ({ onGenerate, isGenerating }) => {
    // Component logic
};

// Use descriptive names
const handleAwardGeneration = async () => {
    // Implementation
};

// Use optional chaining
const awardName = draft?.awardName ?? 'Unknown';

// Use const for values that don't change
const MAX_FILE_SIZE = 10 * 1024 * 1024;
```

**Linting:**
- Run `pnpm lint` to check for issues
- Run `pnpm lint:fix` to auto-fix issues
- Run `pnpm format:fix` to format code with Prettier

### Java Style Guide

**General Principles:**
- Follow Java naming conventions
- Use meaningful class and method names
- Add Javadoc comments for public methods
- Handle exceptions appropriately
- Follow SOLID principles

**Code Formatting:**
```java
// Class names in PascalCase
public class GenerateAwardReactor extends AbstractReactor {
    
    // Constants in UPPER_SNAKE_CASE
    private static final String FILE_NAMES_KEY = "fileNames";
    
    // Method names in camelCase
    public NounMetadata execute() {
        // Implementation
    }
    
    // Proper exception handling
    try {
        processDocument(file);
    } catch (IOException e) {
        classLogger.error("Failed to process document", e);
        throw new SemossPixelException("Document processing failed");
    }
}
```

### Documentation Style Guide

**Markdown Guidelines:**
- Use clear, concise language
- Include code examples where helpful
- Add screenshots for UI-related documentation
- Keep line length reasonable (80-100 characters)
- Use proper heading hierarchy
- Include table of contents for long documents

**Code Comments:**
- Comment "why" not "what"
- Keep comments up to date with code changes
- Use JSDoc/Javadoc for public APIs
- Remove commented-out code before committing

---

## Development Setup

### Frontend Development

**File Structure:**
```
assets/client/src/
├── components/       # React components
├── pages/           # Page components
├── stores/          # MobX stores
├── assets/          # Static assets
└── App.tsx          # Root component
```

**Key Technologies:**
- React 17 with functional components
- MobX for state management
- Material UI for components
- TypeScript for type safety

**Development Commands:**
```bash
pnpm dev          # Start dev server
pnpm build        # Build for production
pnpm lint         # Check for linting errors
pnpm lint:fix     # Fix linting errors
pnpm format:fix   # Format code with Prettier
pnpm type-check   # Run TypeScript type checking
```

### Backend Development

**File Structure:**
```
assets/awards-generator-be/src/main/java/
└── awardsgenerator/
    ├── reactor/     # SEMOSS reactors
    └── util/        # Utility classes
```

**Key Components:**
- SEMOSS Reactors for backend logic
- Apache POI for document parsing
- PDFBox for PDF processing

**Build Commands:**
```bash
mvn clean install      # Build project
mvn clean package      # Create JAR file
mvn test               # Run tests
```

---

## Testing

### Frontend Testing
```bash
# Run all tests
pnpm test

# Run tests in watch mode
pnpm test:watch

# Generate coverage report
pnpm test:coverage
```

### Backend Testing
```bash
# Run all tests
mvn test

# Run specific test class
mvn test -Dtest=GenerateAwardReactorTest

# Run with coverage
mvn clean test jacoco:report
```

### Manual Testing Checklist
- [ ] Test with different award types
- [ ] Test file upload functionality
- [ ] Test with and without uploaded files
- [ ] Test feedback and regeneration
- [ ] Test draft saving and loading
- [ ] Test version navigation
- [ ] Test copy to clipboard
- [ ] Test on different browsers (Chrome, Firefox, Safari, Edge)
- [ ] Test responsive design on mobile devices
- [ ] Test error handling for edge cases

---

## Community

### Getting Help

If you need help with your contribution:
- Check the [documentation](README.md)
- Review existing issues and pull requests
- Ask questions in issue comments
- Contact the maintainers

### Recognition

Contributors will be recognized in:
- The project's contributors list
- Release notes (for significant contributions)
- The acknowledgments section of the README

---

Thank you for contributing to the Award Generator! Your efforts help make this tool better for everyone at the Defense Health Agency.

**Questions?** Feel free to reach out to the project maintainers.
