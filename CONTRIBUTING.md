# Contributing to Movie Recommender System

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the Movie Recommender System project.

## 📝 Code of Conduct

We are committed to providing a welcoming and inspiring community for all. Please be respectful and constructive in all interactions.

## 🐛 Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, include as many details as possible:

- **Use a clear, descriptive title**
- **Describe the exact steps which reproduce the problem**
- **Provide specific examples to demonstrate the steps**
- **Describe the behavior you observed after following the steps**
- **Explain which behavior you expected to see instead and why**
- **Include screenshots/error messages if possible**
- **Include your Python version and OS**

## 💡 Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Use a clear, descriptive title**
- **Provide a step-by-step description of the suggested enhancement**
- **Provide specific examples to demonstrate the steps**
- **Describe the current behavior vs. expected behavior**
- **Explain why this enhancement would be useful**

## 🚀 Pull Request Process

1. **Fork the repository** and create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** with clear, descriptive commits:
   ```bash
   git commit -m "Add brief description of changes"
   ```

3. **Follow the coding standards** (see below)

4. **Test your changes thoroughly**

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request** with:
   - A clear title and description
   - Reference to related issues
   - List of changes made
   - Screenshots/examples if applicable

7. **Respond to review feedback** and make requested changes

## 💻 Development Setup

### Prerequisites
- Python 3.8+
- pip or conda
- Jupyter Notebook

### Setup Steps

1. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/Movie-Recommender-System.git
   cd Movie-Recommender-System
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   pip install -r requirements-dev.txt
   ```

## 📋 Coding Standards

- **Style Guide**: Follow PEP 8
- **Naming Conventions**:
  - Functions/variables: `snake_case`
  - Classes: `PascalCase`
  - Constants: `UPPER_SNAKE_CASE`

- **Documentation**:
  - Write docstrings for all functions and classes
  - Use Google-style docstrings
  - Add comments for complex logic

- **Example Function**:
  ```python
  def calculate_similarity(vector1, vector2):
      """
      Calculate cosine similarity between two vectors.
      
      Args:
          vector1 (np.ndarray): First feature vector
          vector2 (np.ndarray): Second feature vector
          
      Returns:
          float: Cosine similarity score [0, 1]
          
      Raises:
          ValueError: If vectors have different dimensions
      """
      if len(vector1) != len(vector2):
          raise ValueError("Vectors must have same dimensions")
      
      # Calculate similarity
      return dot_product(vector1, vector2) / (norm(vector1) * norm(vector2))
  ```

## ✅ Testing Guidelines

- Write tests for new features
- Ensure existing tests pass: `pytest tests/`
- Aim for >80% code coverage
- Test both success and failure cases

## 📚 Documentation

- Update README.md if adding features
- Add docstrings to all new functions
- Comment complex algorithms
- Update CHANGELOG.md with your changes

## 📝 Commit Message Guidelines

Format: `<type>(<scope>): <subject>`

**Types**:
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, semicolons, etc.)
- `refactor`: Code refactoring without feature changes
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Build process, dependencies, etc.

**Examples**:
```
feat(recommender): Add hybrid filtering algorithm
fix(similarity): Correct cosine similarity calculation
docs(readme): Update installation instructions
```

## 🔄 Branching Strategy

- `main`: Stable, production-ready code
- `develop`: Development branch for integration
- `feature/name`: Feature branches
- `bugfix/name`: Bug fix branches
- `docs/name`: Documentation branches

## 🎯 Priority Guidelines

Issues are labeled by priority:
- `priority-critical`: Urgent, affects core functionality
- `priority-high`: Important, should be addressed soon
- `priority-medium`: Can be addressed in regular sprint
- `priority-low`: Nice to have, can wait

## 📞 Questions?

- Check existing issues and discussions
- Open a new discussion for questions
- Review documentation first

## ⭐ Recognition

Contributors will be:
- Listed in README contributors section
- Recognized in release notes
- Appreciated for their valuable input!

---

Thank you for contributing! 🙌
