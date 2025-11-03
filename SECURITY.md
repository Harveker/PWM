# Security Policy

## Reporting Security Issues

If you discover a security vulnerability within this project, please send an email to the repository maintainer through GitHub's private security advisory feature. All security vulnerabilities will be promptly addressed.

## Development Security Guidelines

### Personal Information Protection

1. **Never commit personal information** such as:
   - Real names in source code comments
   - Personal email addresses
   - Phone numbers
   - Physical addresses
   - Social media handles

2. **Use GitHub's privacy features**:
   - Configure your Git email to use GitHub's no-reply email: `username@users.noreply.github.com`
   - Enable email privacy in GitHub settings

3. **Review commits before pushing**:
   - Always review your changes with `git diff` before committing
   - Check commit author information with `git log`

### Credentials and Secrets

1. **Never commit**:
   - API keys or tokens
   - Passwords or passphrases
   - Private keys or certificates
   - Database connection strings
   - Any other credentials

2. **Use environment variables** for sensitive configuration
3. **Use .gitignore** to prevent accidental commits of sensitive files

### IDE and System Paths

1. **Avoid absolute paths** in configuration files
2. **Use relative paths** or environment variables
3. **Use generic tool references** instead of specific system paths

### Safe Practices

1. Keep your `.gitignore` file up to date
2. Regularly audit your repository for sensitive information
3. Use GitHub's secret scanning feature
4. Review pull requests for security issues
5. Keep dependencies updated

## Protected Information in This Repository

- Git commit history may contain historical email addresses that cannot be changed without rewriting history
- Configure your local Git client to use privacy-preserving email addresses for future commits

## Changing Your Git Configuration

To protect your privacy in future commits:

```bash
# Set your email to GitHub's no-reply address
git config user.email "username@users.noreply.github.com"

# Or set it globally
git config --global user.email "username@users.noreply.github.com"
```
