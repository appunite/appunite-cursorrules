# Awesome .cursorrules by Appunite

A curated list of awesome `.cursorrules` files for enhancing your Cursor AI experience by [Appunite](https://www.appunite.com/).

Cursor is an AI-powered code editor. `.cursorrules` files define custom rules for Cursor to follow when generating code, allowing you to tailor its behavior to your specific needs and preferences.

## 📁 Directory Structure

```
appunite-cursorrules/
├── elixir/                          # Elixir & Phoenix specific rules
│   ├── 02-engineering-principles.mdc    # Core engineering principles & best practices
│   ├── elixir-logger.mdc               # Logger configuration & structured logging
│   ├── elixir-use-vs-import.mdc        # When to use `use` vs `import`
│   ├── live_react.mdc                  # LiveReact integration guidelines
│   └── phoenix-generators.mdc          # Phoenix framework generators usage
├── general/                         # Language-agnostic rules
│   ├── 01-protocol.mdc                 # Project protocol & operational guidelines
│   ├── 03-commit-message-generation-rule.mdc  # Conventional commit messages
│   └── self_improve.mdc                # Guidelines for improving .cursorrules
└── README.md                        # This file
```

## 🚀 Quick Start

1. **Choose your rules**: Browse the directories above to find rules relevant to your project
2. **Copy to your project**: Copy the `.mdc` files you need to your project's `.cursor/` directory
3. **Customize**: Modify the rules to match your specific project requirements
4. **Start coding**: Cursor AI will now follow your custom rules when generating code

## 📋 Available Rules

### 🧪 Elixir & Phoenix Rules

#### `02-engineering-principles.mdc`
**Core engineering principles and best practices for Elixir/Phoenix development**
- Domain-Driven Design patterns
- Functional programming principles
- Phoenix framework best practices
- Testing strategies and patterns
- Error handling conventions
- Code quality guidelines

#### `elixir-logger.mdc`
**Structured logging configuration and usage patterns**
- Logger configuration requirements
- Structured logging best practices
- Metadata vs message content guidelines
- Environment-specific configurations
- Common logging patterns for APIs, databases, and business logic

#### `elixir-use-vs-import.mdc`
**Guidelines for when to use `use` vs `import` in Elixir**
- Phoenix LiveView and Component setup
- Plug.Conn usage patterns
- Decision-making guide with examples
- Common anti-patterns to avoid
- Module behavior adoption vs function importing

#### `live_react.mdc`
**Official LiveReact implementation guidelines**
- Official package usage (avoiding unofficial forks)
- Component syntax and props handling
- Event callbacks and state management
- Asset pipeline configuration
- Migration guides from unofficial packages

#### `phoenix-generators.mdc`
**Phoenix framework generators usage guide**
- Database and schema operations
- Context and business logic generation
- Web interface generation (HTML, JSON, LiveView)
- Real-time communication setup
- Best practices and workflow patterns

### 🌐 General Rules

#### `01-protocol.mdc`
**Project protocol and operational guidelines**
- Context initialization procedures
- Task breakdown methodology (MECE)
- Code change safety requirements
- Priority systems and modes
- AI-first development approach

#### `03-commit-message-generation-rule.mdc`
**Conventional commit message guidelines**
- Commit message structure and types
- Scope and description formatting
- Body and footer conventions
- Breaking change documentation
- Issue tracker integration

#### `self_improve.mdc`
**Guidelines for continuously improving .cursorrules**
- Rule improvement triggers
- Pattern recognition processes
- Quality checks and maintenance
- Documentation update procedures
- Rule deprecation guidelines

## 🎯 Why `.cursorrules`?

`.cursorrules` is a powerful feature in Cursor that allows developers to define project-specific instructions for the AI. Here's why you might want to use it:

*   **🎨 Customized AI Behavior**: `.cursorrules` files help tailor the AI's responses to your project's specific needs, ensuring more relevant and accurate code suggestions.

*   **📏 Consistency**: By defining coding standards and best practices in your `.cursorrules` file, you can ensure that the AI generates code that aligns with your project's style guidelines.

*   **🧠 Context Awareness**: You can provide the AI with important context about your project, such as commonly used methods, architectural decisions, or specific libraries, leading to more informed code generation.

*   **⚡ Improved Productivity**: With well-defined rules, the AI can generate code that requires less manual editing, speeding up your development process.

*   **👥 Team Alignment**: For team projects, a shared `.cursorrules` file ensures that all team members receive consistent AI assistance, promoting cohesion in coding practices.

*   **📚 Project-Specific Knowledge**: You can include information about your project's structure, dependencies, or unique requirements, helping the AI to provide more accurate and relevant suggestions.

By creating a `.cursorrules` file in your project's root directory, you can leverage these benefits and enhance your coding experience with Cursor AI.

## 🛠️ Usage Instructions

### Basic Setup
1. Create a `.cursor/` directory in your project root
2. Copy relevant `.mdc` files from this repository
3. Rename them to `.cursorrules` (remove the `.mdc` extension)
4. Restart Cursor to load the new rules

### Advanced Configuration
- **Combine rules**: You can combine multiple rule files into a single `.cursorrules` file
- **Customize globs**: Modify the `globs` field to target specific file types
- **Set priorities**: Use `alwaysApply: true` for rules that should always be active

### Example Project Structure
```
your-project/
├── .cursor/
│   ├── .cursorrules                 # Main rules file
│   ├── elixir-specific.cursorrules  # Language-specific rules
│   └── team-conventions.cursorrules # Team-specific guidelines
├── lib/
├── test/
└── mix.exs
```

## 🤝 Contributing

We welcome contributions to improve and expand this collection of `.cursorrules` files!

### How to Contribute
1. **Fork** this repository
2. **Create** a new branch for your feature/improvement
3. **Add** your `.cursorrules` file with proper documentation
4. **Test** your rules in a real project
5. **Submit** a pull request with a clear description

### Contribution Guidelines
- Follow the existing file naming conventions
- Include comprehensive documentation and examples
- Test rules with real-world scenarios
- Add appropriate `globs` and `alwaysApply` settings
- Update this README with your new rules

### Rule Quality Standards
- **Actionable**: Rules should provide clear, actionable guidance
- **Specific**: Avoid vague or overly general instructions
- **Tested**: Rules should be tested in actual development scenarios
- **Documented**: Include examples and rationale for each rule

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🏢 About Appunite

[Appunite](https://www.appunite.com/) is a software development company specializing in Product development and modern web/mobile technologies. We're passionate about developer productivity and AI-assisted development.

---

These are the files we use in our daily lives to speed up the development experience. Happy coding! 🚀
