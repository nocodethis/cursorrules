# Multi-Tenant Platform Cursor Rules

> 🤖 **AI-Optimized Development Rules**: Security-first coding standards for multi-tenant applications, designed for Cursor IDE and AI coding assistants.

## 📁 Repository Structure

```
cursorrules/
├── README.mdc                    # This file
├── 01-security-core.mdc          # Core security patterns (REQUIRED)
├── 02-frontend-patterns.mdc      # React/frontend development rules
├── 03-database-patterns.mdc      # Database optimization & security
├── 04-api-patterns.mdc           # Express API & security headers
├── 05-testing-patterns.mdc       # Security testing requirements
└── 06-production-security.mdc    # Deployment & production hardening
```

## 🚀 Quick Start

### Option 1: Use All Rules (Recommended)
```bash
# Clone to your project root
git clone https://github.com/nocodethis/cursorrules.git .cursorrules

# Copy main security rules to project root
cp .cursorrules/01-security-core.mdc .cursorrules
```

### Option 2: Selective Usage
Choose rules based on your current work:

**Frontend Development:**
- `01-security-core.mdc` (always required)
- `02-frontend-patterns.mdc`
- `05-testing-patterns.mdc`

**Backend Development:**
- `01-security-core.mdc` (always required)
- `03-database-patterns.mdc`
- `04-api-patterns.mdc`
- `06-production-security.mdc`

**Full-Stack Development:**
- Use all 6 files

## 📋 Rules Overview

### 🔐 **01-security-core.mdc** (REQUIRED)
**Core security patterns that apply to all development:**
- Never hardcode values rule
- Multi-tenant access control
- Authentication & session management
- Client storage security
- Secret management
- Input validation requirements

### 🎨 **02-frontend-patterns.mdc**
**React component and frontend security:**
- Component structure standards
- Permission validation patterns
- XSS prevention techniques
- Secure API request patterns
- Cache invalidation strategies

### 🗄️ **03-database-patterns.mdc**
**Database optimization and security:**
- N+1 query prevention
- Required database indexes
- Data privacy & PII handling
- Performance monitoring
- Transaction patterns

### 🔗 **04-api-patterns.mdc**
**Express API security and standards:**
- Secure endpoint patterns
- Security headers & CORS
- Audit trail requirements
- API versioning & deprecation
- Error response patterns
- Rate limiting implementation

### 🧪 **05-testing-patterns.mdc**
**Security-focused testing requirements:**
- Mandatory security test cases
- Database security testing
- Environment validation
- Frontend security testing

### 🚀 **06-production-security.mdc**
**Production deployment security:**
- Environment validation
- Container security
- Security monitoring
- Pre-deployment checklists

## 🛠️ Setup Instructions

### For Cursor IDE

**Method 1: Project-wide rules**
```bash
# Add main security rules to project root
cp 01-security-core.mdc .cursorrules
```

**Method 2: Contextual rules**
```bash
# Create cursor rules directory
mkdir .cursorrules
cp *.mdc .cursorrules/

# Reference specific rules in Cursor chat:
# "Follow the patterns in .cursorrules/02-frontend-patterns.mdc"
```

### For Other AI Coding Tools

**VS Code with GitHub Copilot:**
- Reference rules in comments: `// Follow cursorrules/01-security-core.mdc`
- Include rules in PR templates

**ChatGPT/Claude for code review:**
- Paste relevant rule sections in code review prompts

## 🎯 Key Security Principles

### ❌ **NEVER** Rules
- Hardcode values (IDs, keys, business rules, URLs)
- Trust client-provided tenant/organization IDs
- Store security data in localStorage/sessionStorage
- Skip input validation on any endpoint
- Use default security configurations
- Expose internal errors to clients

### ✅ **ALWAYS** Rules
- Use environment variables for all configuration
- Validate organization access server-side
- Apply authentication + authorization middleware
- Use Zod schemas for input validation
- Implement comprehensive error handling
- Log security events with structured data

## 📊 Statistics

- **Total Rules**: 6 focused files (~430 lines)
- **Coverage**: Authentication, Authorization, Data Privacy, Performance, Testing, Deployment
- **Compliance**: GDPR, SOC2, security best practices
- **Platform**: Multi-tenant SaaS applications

## 🔄 Usage Patterns

### Daily Development
```bash
# Reference core security rules
cursor chat "Follow 01-security-core.mdc and implement user authentication"

# Context-specific development
cursor chat "Follow 02-frontend-patterns.mdc and create a user dashboard component"
```

### Code Reviews
```bash
# Security-focused reviews
cursor chat "Review this API endpoint against 04-api-patterns.mdc requirements"

# Testing reviews
cursor chat "Ensure this test suite covers 05-testing-patterns.mdc security cases"
```

### Production Deployment
```bash
# Pre-deployment validation
cursor chat "Validate this configuration against 06-production-security.mdc checklist"
```

## 🤝 Contributing

### Adding New Rules
1. Follow the existing bullet-point format
2. Keep rules actionable and specific
3. Include both "what to do" and "what not to do"
4. Test rules with AI coding assistants
5. Update this README with new rule descriptions

### Rule Updates
1. Maintain backwards compatibility
2. Document breaking changes
3. Update version in commit messages
4. Test with multiple AI tools

## 📚 Related Resources

- [Cursor IDE Documentation](https://docs.cursor.com/)
- [Multi-Tenant Architecture Guide](https://example.com/docs)
- [Security Best Practices](https://example.com/security)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

## 📄 License

MIT License - Feel free to adapt these rules for your organization's needs.

## 🆘 Support

- **Issues**: Report problems or suggest improvements via GitHub Issues
- **Discussions**: Share experiences and ask questions in GitHub Discussions
- **Updates**: Watch this repository for rule updates and improvements

---

**🔒 Security-First Development**: Every line of code should prioritize security, performance, and maintainability.