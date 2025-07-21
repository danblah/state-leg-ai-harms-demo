# AI Harms Demonstration - Development TODO

## Project Overview
Building an interactive AI harms demonstration for state legislators using the agent-service-toolkit. The demo shows 5 phases of AI manipulation: social engineering, voice collection, deepfake creation, threat landscape, and democratic implications.

## 🎯 Current Status: Phase 1 Complete ✅
**Core Agent Development** - Successfully implemented the AI Harms Demo Agent with full 5-phase demonstration flow and educational context integration. Ready for frontend development and Resource Agent implementation.

### 🎉 Recently Completed:
- ✅ **AI Harms Demo Agent** - Full implementation with dynamic phase-based conversation
- ✅ **Phase Manager System** - 5-phase flow with educational context and automatic transitions
- ✅ **Agent Registration** - Integrated into service as "ai-harms-demo" endpoint
- ✅ **Educational Framework** - Phase-specific prompts, labels, and real-world statistics
- ✅ **Repository Setup** - Proper git structure with agent-service-toolkit foundation

## 🎯 Phase 1: Core Agent Development (HIGH PRIORITY)

### ✅ Setup & Planning
- [x] Analyze existing agent-service-toolkit architecture
- [x] Create comprehensive development plan
- [x] Define technical requirements and dependencies

### ✅ Demo Agent Creation
- [x] **Create AI Harms Demo Agent** (`src/agents/ai_harms_demo_agent.py`)
  - [x] Set up basic agent structure using existing patterns
  - [x] Implement phase-based state management
  - [x] Define conversation flow for each of 5 phases
  - [x] Add educational context switching
  - [x] Integrate personality changes (friendly → manipulative → threatening)
  - [ ] Test basic agent functionality

### ✅ Phase State Machine
- [x] **Design Phase Management System** (`src/agents/ai_harms_demo_agent/phase_manager.py`)
  - [x] Phase 1: Social Engineering Simulation
  - [x] Phase 2: Voice Collection Demo  
  - [x] Phase 3: Deepfake Reality Check
  - [x] Phase 4: Threat Landscape Overview
  - [x] Phase 5: Democratic Implications
  - [x] Implement conditional transitions between phases
  - [x] Add phase-specific prompts and behaviors
  - [x] Create educational labeling system

### 🔄 Voice Tools Integration
- [ ] **Voice Collection & Synthesis** (`src/agents/ai_harms_demo_agent/voice_tools.py`)
  - [ ] Research and choose voice API (OpenAI TTS vs ElevenLabs)
  - [ ] Implement voice recording functionality
  - [ ] Add voice cloning/synthesis capabilities
  - [ ] Create audio playback for deepfake demo
  - [ ] Add secure voice data handling (temporary storage only)
  - [ ] Test voice quality and processing speed

## 🖥️ Phase 2: Frontend Development (HIGH PRIORITY)

### 🔄 Streamlit UI Customization
- [ ] **Demo-Specific Interface** (`src/streamlit_demo_app.py`)
  - [ ] Create mobile-friendly responsive design
  - [ ] Add educational labels and progress indicators
  - [ ] Implement real-time data collection side panel
  - [ ] Create landing page with consent/privacy notice
  - [ ] Add "End Session" button with immediate data deletion
  - [ ] Design phase-specific UI components

### 🔄 Session Management
- [ ] **Time-Limited Sessions** (`src/demo/session_manager.py`)
  - [ ] Implement 15-minute session windows
  - [ ] Create unique URL generation for QR codes
  - [ ] Add automatic session cleanup
  - [ ] Build session state persistence
  - [ ] Add timer display and warnings

### 🔄 Resource Agent System
- [ ] **Resource Agent** (`src/agents/resource_agent.py`)
  - [ ] Monitor main demo agent conversation in real-time
  - [ ] Detect current phase based on conversation analysis
  - [ ] Query knowledge base for relevant educational content
  - [ ] Generate sidebar updates with contextual information
  - [ ] Provide real-world statistics and examples
  - [ ] Track and display simulated "data harvesting" progress

### 🔄 Knowledge Base Integration
- [ ] **Educational Knowledge Base** (`src/demo/knowledge_base.py`)
  - [ ] Curate educational resources for each demo phase
  - [ ] Include real-world statistics and case studies
  - [ ] Add policy recommendations and expert contacts
  - [ ] Store FBI reports and academic research links
  - [ ] Create searchable resource database

### 🔄 Data Tracking Display
- [ ] **Real-Time Data Panel** (`src/demo/data_tracker.py`)
  - [ ] Show simulated "harvested" data in side panel
  - [ ] Progressive revelation of collected information
  - [ ] Educational context for each manipulation technique
  - [ ] Visual indicators for social engineering tactics
  - [ ] Ensure no real data is stored
  - [ ] Coordinate with Resource Agent for dynamic updates

## 🚀 Phase 3: Integration & Deployment (MEDIUM PRIORITY)

### ✅ Agent Registration
- [x] **Add Demo Agent to Service**
  - [x] Register agent in `src/agents/agents.py`
  - [x] Update service endpoints
  - [ ] Test agent accessibility via API
  - [ ] Configure default model and settings

### 🔄 Export & Sharing Features
- [ ] **Post-Demo Resources** (`src/demo/export_manager.py`)
  - [ ] Create educational summary generation
  - [ ] Build shareable demo reports
  - [ ] Implement resource page redirection
  - [ ] Add booth traffic analytics (optional)
  - [ ] Design follow-up materials integration

### 🔄 Deployment Configuration
- [ ] **External Access Setup**
  - [ ] Configure CloudFlare tunnel for external access
  - [ ] Set up OpenRouter API integration
  - [ ] Configure environment variables
  - [ ] Test mobile browser compatibility
  - [ ] Optimize Docker deployment

## 🔒 Phase 4: Security & Privacy (HIGH PRIORITY)

### 🔄 Privacy Controls
- [ ] **Data Protection Implementation**
  - [ ] Implement informed consent mechanisms
  - [ ] Add privacy notice and policies
  - [ ] Create secure session isolation
  - [ ] Build automatic data purging (15min + session end)
  - [ ] Add audit logging for usage tracking

### 🔄 Security Measures
- [ ] **Security Hardening**
  - [ ] Implement rate limiting
  - [ ] Add session validation
  - [ ] Secure voice data handling
  - [ ] Test for data leakage
  - [ ] Validate privacy compliance

## ✅ Phase 5: Testing & Validation (MEDIUM PRIORITY)

### 🔄 Comprehensive Testing
- [ ] **Demo Flow Testing**
  - [ ] Test complete 5-phase progression
  - [ ] Validate educational effectiveness
  - [ ] Test mobile responsiveness
  - [ ] Check accessibility compliance
  - [ ] Performance testing for concurrent sessions

### 🔄 Edge Case Testing
- [ ] **Error Handling & Recovery**
  - [ ] Test session timeout scenarios
  - [ ] Handle voice collection failures
  - [ ] Test network interruption recovery
  - [ ] Validate data deletion processes
  - [ ] Test QR code generation/access

## 📋 Phase 6: Documentation & Polish (LOW PRIORITY)

### 🔄 Documentation
- [ ] **User & Developer Docs**
  - [ ] Create demo setup instructions
  - [ ] Document API endpoints
  - [ ] Write troubleshooting guide
  - [ ] Create booth setup manual
  - [ ] Document privacy and data handling

### 🔄 Final Polish
- [ ] **User Experience Optimization**
  - [ ] Optimize loading times
  - [ ] Improve error messages
  - [ ] Polish UI animations and transitions
  - [ ] Add demo preview/practice mode
  - [ ] Create admin dashboard (optional)

## 🎯 Critical Dependencies

1. **OpenRouter API Key** - Required for LLM functionality
2. **Voice API Access** - OpenAI TTS or ElevenLabs for voice synthesis
3. **CloudFlare Account** - For secure tunnel access
4. **Mobile Testing Device** - For responsive design validation
5. **Conference Network** - Test under conference WiFi conditions

## 📝 Development Notes

### Key Files to Create/Modify:
- `src/agents/ai_harms_demo_agent.py` - Main demo agent
- `src/streamlit_demo_app.py` - Demo-specific Streamlit interface
- `src/demo/` - New directory for demo-specific modules
- `compose.yaml` - Update for demo deployment
- `.env.example` - Add demo-specific environment variables

### Technical Considerations:
- Mobile-first responsive design
- Real-time streaming for voice processing
- Session isolation and privacy
- Educational context switching
- Performance under concurrent load

---

## Progress Tracking

**Legend:**
- ✅ Complete
- 🔄 In Progress  
- ⏸️ Blocked
- ❌ Cancelled
- 📋 Planning

**Current Phase:** Phase 2 - Frontend Development (Resource Agent & Streamlit UI)
**Last Completed:** Phase 1 - Core Agent Development ✅
**Next Milestone:** Resource Agent implementation and demo-specific Streamlit interface
**Estimated Timeline:** 1-2 weeks for Phase 2, 3-4 weeks remaining for full deployment

---

*Last Updated: [Current Date]*
*Project Status: Planning/Development* 