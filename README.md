# 🐛 Zero Hour

> Transform debugging from frustration to mastery. A comprehensive platform where developers sharpen their debugging skills through real-world challenges, AI-powered guidance, and competition-based hiring opportunities.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Status: In Development](https://img.shields.io/badge/Status-In%20Development-blue.svg)]()

## 🎯 Vision

The Developer Debugging Platform is the **"LeetCode for debugging"** - a gamified learning environment where developers of all skill levels can practice debugging real-world issues in safe, isolated virtual environments. With AI-powered Socratic guidance and competition-based hiring, we're revolutionizing how developers learn and how companies discover talent.

## ✨ Key Features

### 🌍 Universal Language Support
- **All Major Languages**: JavaScript, TypeScript, Python, Java, C#, Go, Rust, PHP, Ruby, and more
- **Popular Frameworks**: React, Vue, Angular, Flask, Django, Spring Boot, .NET Core, Express.js
- **Any Bug Type**: Logic errors, performance issues, security vulnerabilities, memory leaks, race conditions

### 🤖 AI-Powered Socratic Guidance
- **Intelligent Mentorship**: AI that teaches through questions, not answers
- **NotebookLM Integration**: Dynamic educational content generation
- **Context-Aware Hints**: Progressive guidance that adapts to your skill level
- **Methodology Teaching**: Learn systematic debugging approaches

### 🏆 Competition-Based Hiring
- **Live Debugging Contests**: Company-hosted competitions with real job opportunities
- **Real-Time Leaderboards**: Compete against developers worldwide
- **Winner-Takes-Job**: Top performers secure direct job offers
- **Skill Verification**: Demonstrate abilities through practical challenges

### 📊 Comprehensive Analytics
- **Progress Tracking**: Monitor your growth across languages and bug types
- **Skill Radar Charts**: Visualize your debugging proficiency
- **Peer Benchmarking**: Compare your performance anonymously
- **Exportable Portfolios**: Showcase your skills to potential employers

### 🔧 Virtual Environments
- **Isolated Containers**: Safe experimentation without local setup
- **Pre-Configured Stacks**: Everything you need, ready to go
- **Full Development Tools**: Code editor, debugger, terminal access
- **Multi-Service Support**: Debug complex applications and microservices

### 🎓 Real-World Challenges
- **GitHub Integration**: Automated curation from 1000+ popular repositories
- **AI Complexity Rating**: Intelligent difficulty assessment
- **Authentic Scenarios**: Learn from actual production bugs
- **Continuous Updates**: New challenges added regularly

## 🚀 Getting Started

### For Students & Developers

1. **Sign Up**: Create your free account
2. **Choose Your Path**: Select challenges based on your skill level and interests
3. **Start Debugging**: Launch virtual environments and solve real-world bugs
4. **Get AI Guidance**: Ask questions and receive Socratic hints
5. **Track Progress**: Monitor your skill development and earn achievements
6. **Compete**: Join competitions and showcase your abilities

### For Companies & Recruiters

1. **Create Company Profile**: Set up your organization account
2. **Host Competitions**: Design custom debugging challenges
3. **Discover Talent**: Search for developers with specific skills
4. **Assess Candidates**: Review detailed performance analytics
5. **Hire Winners**: Make direct job offers to top performers

## 🏗️ Architecture

### Technology Stack

**Frontend:**
- Next.js 14 with React 18
- Tailwind CSS + shadcn/ui
- Monaco Editor (VS Code engine)
- Socket.io for real-time features

**Backend:**
- Node.js microservices with TypeScript
- Python FastAPI for AI services
- Express.js with Passport.js
- Kong API Gateway

**Infrastructure:**
- Kubernetes for container orchestration
- Docker for virtual environments
- PostgreSQL, MongoDB, Redis, InfluxDB
- AWS/Azure cloud hosting

**AI & ML:**
- OpenAI GPT-4 for guidance
- NotebookLM API for content generation
- Custom ML models for complexity rating
- Pinecone vector database

### System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        CDN Layer                            │
│                  (CloudFlare/AWS CloudFront)               │
└────────────────────────┬────────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────────┐
│                    API Gateway                              │
│              (Kong + Rate Limiting)                         │
└────────────────────────┬────────────────────────────────────┘
                         │
        ┌────────────────┼────────────────┐
        │                │                │
┌───────▼──────┐  ┌─────▼──────┐  ┌─────▼──────┐
│   Frontend   │  │Microservices│  │  External  │
│   (Next.js)  │  │  Ecosystem  │  │Integrations│
└──────────────┘  └─────┬──────┘  └────────────┘
                        │
        ┌───────────────┼───────────────┐
        │               │               │
┌───────▼──────┐ ┌─────▼──────┐ ┌─────▼──────┐
│  Challenge   │ │   Virtual  │ │     AI     │
│   Service    │ │Environment │ │  Guidance  │
└──────────────┘ └────────────┘ └────────────┘
```

## 📚 Documentation

- **[Requirements](/.kiro/specs/developer-debugging-platform/requirements.md)**: Detailed user stories and acceptance criteria
- **[Design Document](/.kiro/specs/developer-debugging-platform/design.md)**: Comprehensive technical architecture
- **[API Documentation](#)**: Coming soon
- **[User Guide](#)**: Coming soon

## 🛠️ Development Setup

### Prerequisites

- Node.js 18+ and npm/yarn
- Python 3.9+
- Docker and Docker Compose
- Kubernetes (minikube for local development)
- PostgreSQL 14+
- Redis 7+
- MongoDB 6+

### Local Development

```bash
# Clone the repository
git clone https://github.com/your-org/developer-debugging-platform.git
cd developer-debugging-platform

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your configuration

# Start infrastructure services
docker-compose up -d postgres redis mongodb

# Run database migrations
npm run migrate

# Start development servers
npm run dev

# In another terminal, start the AI service
cd services/ai-guidance
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py

# Access the application
# Frontend: http://localhost:3000
# API: http://localhost:8000
# API Docs: http://localhost:8000/docs
```

### Running Tests

```bash
# Run all tests
npm test

# Run unit tests
npm run test:unit

# Run integration tests
npm run test:integration

# Run e2e tests
npm run test:e2e

# Run property-based tests
npm run test:pbt

# Run with coverage
npm run test:coverage
```

## 🤝 Contributing

We welcome contributions from the community! Whether you're fixing bugs, adding features, or improving documentation, your help is appreciated.

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes**: Follow our coding standards
4. **Write tests**: Ensure your code is well-tested
5. **Commit your changes**: `git commit -m 'Add amazing feature'`
6. **Push to the branch**: `git push origin feature/amazing-feature`
7. **Open a Pull Request**: Describe your changes clearly

### Development Guidelines

- Follow the existing code style and conventions
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR
- Keep PRs focused and atomic

### Code of Conduct

We are committed to providing a welcoming and inclusive environment. Please read our [Code of Conduct](CODE_OF_CONDUCT.md) before contributing.

## 🗺️ Roadmap

### Phase 1: MVP (Current)
- [x] Requirements and design documentation
- [ ] Core challenge management system
- [ ] Basic virtual environment support
- [ ] User authentication and profiles
- [ ] Simple AI guidance integration
- [ ] Challenge browser and IDE interface

### Phase 2: Enhanced Features
- [ ] Competition system with real-time leaderboards
- [ ] Advanced AI guidance with NotebookLM
- [ ] Comprehensive analytics dashboard
- [ ] GitHub issue automation
- [ ] Multi-language support expansion
- [ ] Mobile-responsive improvements

### Phase 3: Enterprise & Hiring
- [ ] Company portal and management
- [ ] ATS integrations (Greenhouse, Lever, etc.)
- [ ] Advanced talent discovery
- [ ] Custom assessment creation
- [ ] Team competitions
- [ ] White-label solutions

### Phase 4: Advanced Features
- [ ] Collaborative debugging challenges
- [ ] Mentorship marketplace
- [ ] Certification programs
- [ ] API for third-party integrations
- [ ] Advanced ML-powered recommendations
- [ ] Global debugging tournaments

## 📊 Project Status

| Component | Status | Coverage | Notes |
|-----------|--------|----------|-------|
| Requirements | ✅ Complete | - | Comprehensive user stories |
| Design | ✅ Complete | - | Full technical architecture |
| Frontend | 🚧 In Progress | - | Next.js setup complete |
| Backend Services | 🚧 In Progress | - | Core APIs in development |
| Virtual Environments | 📋 Planned | - | Docker setup in progress |
| AI Guidance | 📋 Planned | - | Integration design complete |
| Database | 🚧 In Progress | - | Schema implemented |
| Testing | 📋 Planned | - | Test framework setup |
| Documentation | 🚧 In Progress | - | API docs in progress |
| Deployment | 📋 Planned | - | Infrastructure design complete |

**Legend:** ✅ Complete | 🚧 In Progress | 📋 Planned | ❌ Blocked

## 🔒 Security

Security is a top priority. We implement:

- **Container Isolation**: Each virtual environment is fully isolated
- **Encryption**: TLS 1.3 for transit, AES-256 for data at rest
- **Authentication**: JWT with refresh tokens, optional 2FA
- **Regular Audits**: Automated security scanning and manual reviews
- **Compliance**: GDPR compliant, SOC 2 Type II certified

### Reporting Security Issues

If you discover a security vulnerability, please email security@debugplatform.com. Do not open public issues for security concerns.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **GitHub**: For providing the API that powers our challenge curation
- **NotebookLM**: For AI-powered educational content generation
- **Open Source Community**: For the amazing tools and libraries we build upon
- **Contributors**: Everyone who has contributed to making this platform better

## 📞 Contact & Support

- **Website**: [https://debugplatform.com](https://debugplatform.com)
- **Email**: support@debugplatform.com
- **Twitter**: [@DebugPlatform](https://twitter.com/DebugPlatform)
- **Discord**: [Join our community](https://discord.gg/debugplatform)
- **GitHub Issues**: [Report bugs or request features](https://github.com/your-org/developer-debugging-platform/issues)

## 🌟 Star History

If you find this project useful, please consider giving it a star! ⭐

---

**Built with ❤️ by developers, for developers**

*Transforming debugging from a necessary evil into a competitive advantage*
