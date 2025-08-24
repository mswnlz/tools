# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a Chinese tools resource repository (`mswnlz/tools`) that serves as a curated collection of useful software, tools, and resources. The repository includes:

- A simple GitHub Action for notifications (`aiknowledge-action`)
- Monthly resource files containing links to various tools and software
- Multilingual README linking to related projects in the mswnlz ecosystem

## Architecture

### Repository Structure
- `index.js` - Main GitHub Action entry point using @actions/core
- `action.yml` - GitHub Action configuration file
- `package.json` - Node.js dependencies (minimal: only @actions/core)
- `202X0X.md` files - Monthly resource collections (format: YYYYMM.md)
- `README.md` - Multilingual project description with ecosystem links

### GitHub Action Component
The repository contains a minimal GitHub Action called "AIknowledge Notify" that:
- Takes a message input parameter (optional, defaults to "Hello from AIknowledge Action!")
- Uses Node.js 16 runtime
- Simply prints the provided message to console
- Handles errors gracefully using @actions/core.setFailed()

### Monthly Resource Files
Resource files follow a YYYYMM.md naming pattern and contain:
- Categorized tool links (primarily to pan.quark.cn and pan.baidu.com)
- Software tools (Office suites, media editors, development tools)
- Educational resources and tutorials
- Mobile applications and utilities

## Common Commands

### Development
```bash
# Install dependencies
npm install

# Test the action locally (simulate GitHub Action environment)
node index.js
```

### GitHub Action Usage
This action can be used in workflows with:
```yaml
- uses: mswnlz/tools@main
  with:
    message: "Custom notification message"
```

### Resource Management
```bash
# Create new monthly resource file
touch $(date +%Y%m).md

# View recent resource files
ls -la 2025*.md | head -5
```

## Content Guidelines

### Monthly Resource Files
- Use consistent formatting with descriptive titles
- Include proper attribution with "超过100T资料总站网站-doc.869hr.uk" suffix
- Organize resources by category (Office tools, media software, educational content)
- Provide both Chinese and English descriptions where applicable

### Link Management
- Verify all external links are active before committing
- Use consistent URL shortening format (s.869hr.uk for shortened links)
- Include extraction codes for cloud storage links where required

## Ecosystem Integration

This repository is part of a larger project ecosystem including:
- `chinese-traditional` - Traditional Chinese medicine resources
- `cross-border` - Cross-border e-commerce materials
- `self-media` - Social media resources
- `edu-knowledge` - Educational materials
- `AIknowledge` - AI-related knowledge and tutorials
- `curriculum` - Various course materials
- `movies` - Media and entertainment resources
- `book` - Book and literature collections
- `healthy` - Health and fitness resources

## Multilingual Support

The README supports 20+ languages through openaitx.github.io view system:
- Primary: Chinese (Simplified and Traditional)
- Supported: English, Japanese, Korean, Hindi, Thai, French, German, Spanish, Italian, Russian, Portuguese, Dutch, Polish, Arabic, Persian, Turkish, Vietnamese, Indonesian
