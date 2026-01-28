# Contributing to Nexus Auto Trader

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in [Issues](https://github.com/yourusername/nexus-trader/issues)
2. If not, create a new issue with:
   - Clear title describing the bug
   - Steps to reproduce
   - Expected behavior
   - Actual behavior
   - Browser and OS information
   - Screenshots if applicable

### Suggesting Features

1. Check existing issues for similar suggestions
2. Create a new issue with the `enhancement` label
3. Describe the feature and its use case
4. Explain why it would be valuable

### Pull Requests

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Test thoroughly
5. Commit with clear messages: `git commit -m "Add: feature description"`
6. Push to your fork: `git push origin feature/your-feature`
7. Open a Pull Request

## Code Style

### JavaScript
- Use `const` and `let`, avoid `var`
- Use arrow functions where appropriate
- Keep functions small and focused
- Add comments for complex logic

### HTML/CSS
- Use semantic HTML elements
- Keep CSS organized by component
- Use CSS variables for colors/themes
- Mobile-first responsive design

### Commit Messages

Format: `Type: Brief description`

Types:
- `Add:` New feature
- `Fix:` Bug fix
- `Update:` Improvement to existing feature
- `Remove:` Removing code/feature
- `Refactor:` Code restructuring
- `Docs:` Documentation changes
- `Style:` Formatting, no code change

## Development Setup

```bash
# Clone your fork
git clone https://github.com/yourusername/nexus-trader.git
cd nexus-trader

# Open in browser (no build needed)
open index.html

# Or use a local server
npx serve
```

## Testing

Currently, testing is manual:
1. Open the app in browser
2. Test paper trading mode
3. Verify all filters work
4. Check all strategies
5. Test on different screen sizes

## Questions?

Feel free to open an issue with the `question` label.

Thank you for contributing! 🚀
