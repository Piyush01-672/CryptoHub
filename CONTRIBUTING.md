# Contributing to CryptoHub

Thank you for your interest in contributing to CryptoHub! This document provides guidelines and instructions for contributing to the project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Submitting Changes](#submitting-changes)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Pull Request Process](#pull-request-process)
- [Reporting Issues](#reporting-issues)

## Code of Conduct

This project is committed to providing a welcoming and inclusive environment for all contributors. We expect all participants to:

- Be respectful and professional in all interactions
- Welcome diverse perspectives and experiences
- Focus on what is best for the community
- Show empathy towards other community members
- Report unacceptable behavior to the project maintainers

Any behavior that violates these principles will not be tolerated.

## Getting Started

### Prerequisites

- Node.js 14+ and npm
- Git
- A GitHub account

### Setup Development Environment

1. **Fork the repository** on GitHub
2. **Clone your fork:**
   ```sh
   git clone https://github.com/your-username/CryptoHub.git
   cd CryptoHub
   ```
3. **Add upstream remote:**
   ```sh
   git remote add upstream https://github.com/KaranUnique/CryptoHub.git
   ```
4. **Install dependencies:**
   ```sh
   npm install
   ```
5. **Create your `.env` file:**
   ```
   VITE_CG_API_KEY=your-coingecko-api-key
   ```
6. **Start development server:**
   ```sh
   npm run dev
   ```

## Development Workflow

### Branch Naming Conventions

Use descriptive branch names:
- Features: `feature/description`
- Bug fixes: `bugfix/description`
- Documentation: `docs/description`
- Performance: `perf/description`

Example:
```sh
git checkout -b feature/add-portfolio-tracker
```

### Creating Changes

1. **Keep commits atomic** - Each commit should represent one logical change
2. **Write clear commit messages:**
   ```
   [Type]: Brief description
   
   Detailed explanation of changes (if needed)
   ```
   Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

3. **Test your changes locally** before pushing

### Syncing with Upstream

Before creating a Pull Request, sync with the main repository:
```sh
git fetch upstream
git rebase upstream/main
git push origin your-branch-name
```

## Submitting Changes

### Step-by-Step Process

1. **Make your changes** on your feature branch
2. **Test thoroughly** in your local environment
3. **Push to your fork:**
   ```sh
   git push origin feature/your-feature-name
   ```
4. **Open a Pull Request** on the main repository

### Pull Request Checklist

Before submitting, ensure:
- [ ] Your code follows the coding standards
- [ ] You've tested your changes locally
- [ ] You've updated relevant documentation
- [ ] Commit messages are clear and descriptive
- [ ] Your branch is up-to-date with main
- [ ] No unrelated changes are included

## Coding Standards

### General Guidelines

- Use meaningful variable and function names
- Keep functions small and focused (single responsibility)
- Add comments for complex logic
- Use consistent indentation (2 spaces)
- Avoid console.log in production code

### React/JSX Guidelines

- Use functional components with hooks
- Keep components modular and reusable
- Use descriptive component names (PascalCase)
- Keep JSX clean and readable
- Extract complex logic into custom hooks

### CSS Guidelines

- Use consistent naming conventions
- Group related styles together
- Use meaningful class names
- Avoid inline styles
- Ensure responsive design

### Example Code Style

```jsx
// Good
const UserCard = ({ user, onDelete }) => {
  const [expanded, setExpanded] = useState(false);

  const handleToggle = () => {
    setExpanded(!expanded);
  };

  return (
    <div className="user-card">
      <h3>{user.name}</h3>
      <button onClick={handleToggle}>
        {expanded ? 'Collapse' : 'Expand'}
      </button>
    </div>
  );
};

export default UserCard;
```

## Testing

### Local Testing

- Test your changes across different screen sizes
- Test in multiple browsers (Chrome, Firefox, Safari)
- Verify API calls work correctly
- Test with different currencies/data

## Pull Request Process

### Creating a PR

1. Fill out the PR template completely
2. Provide a clear title and description
3. Link related issues if applicable
4. Add labels if available

### PR Template

```markdown
## Description
Brief description of changes

## Related Issue
Closes #(issue number)

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement

## Testing
How was this tested?

## Screenshots
If applicable, add screenshots

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No breaking changes
```

### Review Process

- At least one maintainer review required
- Address feedback constructively
- Update your PR based on review comments
- Maintainers will merge when ready

## Reporting Issues

### Bug Reports

Please include:
- Clear, descriptive title
- Step-by-step reproduction steps
- Expected behavior
- Actual behavior
- Screenshots/error logs
- Browser and OS information

### Feature Requests

Please include:
- Clear, descriptive title
- Why this feature would be useful
- Possible implementation approach
- Any related issues

## Areas We Need Help With

- Bug fixes and performance improvements
- New features and enhancements
- UI/UX improvements
- Documentation and tutorials
- Blog content
- Accessibility improvements
- Testing

## Questions?

- Open a GitHub Issue
- Contact the maintainers
- Check existing discussions

---

Thank you for contributing to CryptoHub! Your help makes this project better for everyone. 🚀
