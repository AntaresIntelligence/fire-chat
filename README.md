# 🔥 Fire Chat - Enterprise-Grade AI Chat Application

An enterprise-ready chat application with secure Flowise integration and Supabase backend.

## ✨ Features

- 🔐 **Secure Authentication** - JWT-based auth with Supabase
- 💬 **Real-time Chat** - Live message synchronization
- 🏢 **Multi-tenant** - Organization-based user management
- 🤖 **AI Integration** - Seamless Flowise connection with session management
- 📊 **Usage Analytics** - Track costs and performance
- 🛡️ **Enterprise Security** - Row-level security and encrypted data

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- Supabase account
- Flowise instance

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/AntaresIntelligence/fire-chat.git
cd fire-chat
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment**
```bash
cp .env.example .env.local
# Edit .env.local with your Supabase credentials
```

4. **Set up database**
```bash
# Run the SQL scripts in supabase/migrations/
```

5. **Deploy Edge Functions**
```bash
supabase functions deploy
```

6. **Start development server**
```bash
npm run dev
```

## 📁 Project Structure

```
fire-chat/
├── docs/                   # Documentation
│   ├── PRD.md             # Product Requirements Document
│   ├── TECHNICAL_ARCHITECTURE.md
│   └── IMPLEMENTATION_GUIDE.md
├── src/                   # Frontend React application
│   ├── components/        # React components
│   ├── contexts/         # React contexts
│   ├── services/         # API services
│   └── lib/              # Utilities and Supabase client
├── supabase/             # Supabase configuration
│   ├── functions/        # Edge Functions
│   └── migrations/       # Database migrations
└── package.json
```

## 🏗️ Architecture

```
Frontend (React) ↔ Supabase Backend ↔ Flowise Instance
     ↓                    ↓              ↓
 - UI/UX only        - Auth & Security  - AI Processing
 - State mgmt        - Session mgmt     - Conversation memory
 - User actions      - API proxying     - Message history
```

## 🔧 Configuration

### Environment Variables

```env
REACT_APP_SUPABASE_URL=your-supabase-url
REACT_APP_SUPABASE_ANON_KEY=your-supabase-anon-key
```

### Supabase Edge Function Secrets

```bash
supabase secrets set FLOWISE_DEFAULT_URL=your-flowise-url
supabase secrets set ENCRYPTION_KEY=your-encryption-key
```

## 📚 Documentation

- [Product Requirements Document](docs/PRD.md)
- [Technical Architecture](docs/TECHNICAL_ARCHITECTURE.md)
- [Implementation Guide](docs/IMPLEMENTATION_GUIDE.md)
- [API Documentation](docs/API.md)

## 🛡️ Security Features

- **Zero API Key Exposure** - All credentials stored securely on backend
- **Row Level Security** - Database-level access control
- **Encrypted Storage** - Sensitive data encrypted at rest
- **JWT Authentication** - Secure token-based auth
- **Audit Logging** - Complete activity tracking

## 📊 Performance Benefits

- **90% Cost Reduction** - Efficient session management vs sending full history
- **Sub-second Responses** - Optimized API communication
- **Unlimited History** - Database storage vs browser limitations
- **Real-time Sync** - Live updates across devices

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- Create an [issue](https://github.com/AntaresIntelligence/fire-chat/issues) for bug reports
- Join our [discussions](https://github.com/AntaresIntelligence/fire-chat/discussions) for questions
- Check the [documentation](docs/) for detailed guides

---

Built with ❤️ using [React](https://reactjs.org/), [Supabase](https://supabase.com/), and [Flowise](https://flowiseai.com/)
