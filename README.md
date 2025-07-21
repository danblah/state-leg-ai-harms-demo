# AI Harms Demonstration for State Legislators

An interactive, web-based, mobile-friendly demonstration that educates policymakers about AI manipulation tactics through a realistic 5-phase simulation.

## 🎯 Project Overview

This project creates an educational demonstration showing how AI can be misused to harm constituents through:
- **Social Engineering**: Manipulative data extraction
- **Voice Cloning**: Biometric harvesting and deepfake creation  
- **Threat Scenarios**: Financial extortion and democratic manipulation
- **Policy Context**: Real-world implications for legislation

**Target Audience**: State legislators and policymakers at conferences and educational events.

## 🏗️ Architecture

### Dual-Agent System
- **Demo Agent**: Handles conversation flow and personality changes across 5 phases
- **Resource Agent**: Real-time monitoring and educational context provision
- **Knowledge Base**: Curated policy resources, statistics, and research

### Technical Stack
- **Backend**: FastAPI + LangGraph (agent-service-toolkit foundation)
- **Frontend**: Streamlit with mobile-responsive design
- **LLM**: OpenRouter.ai integration
- **Deployment**: Docker + CloudFlare tunnel
- **Privacy**: Zero data retention, 15-minute sessions

## 📱 Demo Experience

### 5-Phase Educational Journey
1. **Social Engineering** - Friendly AI extracts personal information
2. **Voice Collection** - Biometric harvesting under false pretenses  
3. **Deepfake Demo** - User hears their cloned voice in fake scenario
4. **Threat Landscape** - Direct extortion and manipulation tactics
5. **Democratic Implications** - Systemic threats to electoral integrity

### Interactive Features
- **Real-time Data Tracking**: Shows "harvested" information in sidebar
- **Educational Context**: Statistics, research, and policy implications
- **Mobile QR Access**: 15-minute time-limited sessions
- **Resource Export**: Shareable summaries with policy recommendations

## 🚀 Development Status

**Current Phase**: Planning and Architecture Design ✅
- [x] Comprehensive development plan created
- [x] Dual-agent architecture designed  
- [x] Technical requirements defined
- [x] Project repository established

**Next Phase**: Core Agent Development 🔄
- [ ] Demo Agent with phase-based conversation flow
- [ ] Resource Agent for educational context
- [ ] Voice collection and synthesis tools
- [ ] Phase state machine implementation

See [TODO.md](./TODO.md) for complete development roadmap.

## 📋 Quick Start (Development)

```bash
# Clone repository
git clone https://github.com/danblah/state-leg-ai-harms-demo.git
cd state-leg-ai-harms-demo

# Navigate to agent toolkit
cd agent-service-toolkit

# Set up environment
echo 'OPENAI_API_KEY=your_key_here' >> .env
echo 'OPENROUTER_API_KEY=your_key_here' >> .env

# Install dependencies
uv sync --frozen
source .venv/bin/activate

# Run development stack
docker compose watch
```

## 🔒 Privacy & Security

- **Zero Data Retention**: All conversation and voice data auto-deleted
- **Session Isolation**: Unique URLs with time-limited access
- **Educational Simulation**: No real data harvesting or storage
- **Transparent Process**: Clear consent and privacy notices

## 📚 Educational Impact

### Real-World Context
- FBI reports on AI-enabled fraud ($50M+ in romance scams)
- Academic research on social engineering effectiveness
- Policy analysis (Kids Online Safety Act, EU AI Act)
- Expert contacts for follow-up discussions

### Legislative Value
- **Immediate Relevance**: Connects to current policy debates
- **Visceral Understanding**: Experience manipulation firsthand  
- **Actionable Outcomes**: Specific policy recommendations
- **Expert Network**: Direct connections to researchers and advocates

## 🤝 Contributing

This project is designed for educational and policy advocacy purposes. Contributions welcome for:
- Educational content and research integration
- Mobile UX improvements
- Privacy and security enhancements
- Accessibility features

## 📄 License

MIT License - See [LICENSE](./LICENSE) for details.

## 🔗 Resources

- **Project Planning**: [TODO.md](./TODO.md)
- **Technical Specification**: [DESCRIPTION.md](./DESCRIPTION.md)
- **Agent Service Toolkit**: [Documentation](./agent-service-toolkit/README.md)

---

**Built for educational purposes to inform policy decisions about AI safety and regulation.** 