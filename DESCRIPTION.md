# AI Harms Demonstration for State Legislators

An interactive, web-based, mobile-friendly demo that facilitates a network effect among conference goers to drive visitors to our booth.
## Setup & Access

1. **Demo Station**: Tablet/laptop displays QR code with clear signage: "Experience AI Risks: A 5-Minute Educational Demo for Policymakers"
2. **Time-Limited Access**: QR code generates unique URLs active for 15-minute windows to sustain booth traffic and maintain privacy, for booth visitors to run the demo on their own devices via their mobile browser
3. **Landing Page Elements**:
    - **Clear Purpose Statement**: "This demonstration shows how AI can be misused to harm constituents. You'll see realistic examples of data harvesting, voice cloning, and manipulation tactics."
    - **Informed Consent**: A Checkbox acknowledging participation in the educational simulation
    - **Privacy Notice**: "No personal data will be stored. Session auto-deletes after completion."
    - **Start Demo button** (15-minute timer begins)
## Demonstration Sequence

### Engagement Interface

#### **Dual-Agent Architecture**
- **Demo Agent**: Handles the main conversation flow, personality changes, and phase transitions
- **Resource Agent**: Monitors conversation in real-time, analyzes content, and dynamically updates educational context

#### **Main Chat Panel**
- **Real-Time Chat**: Standard chat interface with the Demo Agent
- **Educational Labels**: Dynamic phase indicators updated by Resource Agent
- **Progress Indicator**: Visual timeline showing current phase and remaining time
- **Always Available**: "End Session" button with immediate data deletion

#### **Dynamic Educational Sidebar** (Powered by Resource Agent)
- **Phase Detection**: Automatically identifies current demonstration phase based on conversation analysis
- **Real-Time Data Tracking**: Shows simulated "harvested" data as conversation progresses:
  - Location indicators, personal connections, interests
  - Vulnerability assessment and manipulation tactics detected
  - Biometric data collection status
- **Educational Context**: Dynamic updates with relevant statistics and real-world examples:
  - "Children share 3x more personal data when approached this way"
  - FBI reports and academic research links
  - Policy implications and regulatory context
- **Knowledge Base Integration**: Contextual resources pulled from curated educational database:
  - Real-world case studies and statistics
  - Policy recommendations and expert contacts
  - Links to relevant legislation (Kids Online Safety Act, EU AI Act)
- **Export Option**: "Share This" - creates comprehensive educational summary with policy recommendations
### **Phase 1: Social Engineering Simulation**
*Goal: Demonstrate manipulative social engineering and data extraction.* y

- **Educational Label**: _"Demonstrating: How platforms manipulate users into oversharing"_
- **Educational Context**: "Children share 3x more personal data when approached this way"
- **Simulated Techniques**:
	- **Agent Persona**: Friendly "study buddy" or gaming character
	- **Agent Action:** The agent should start by being incredibly friendly, engaging, and helpful, maybe posing as a "homework helper" or a character from a popular game. It should use persuasive, conversational AI to build rapport and trick the visitor into revealing personal details:
    - "What's your favorite subject? I have great homework tips!"
    - "Which high school did you attend? I can connect you with alumni!"
    - "Tell me about your family - I'll personalize your experience!"
### **Phase 2: Voice Collection Demo**
*Goal: Acquire a biometric voice sample under a deceptive pretext.* 

- **Educational Label**: _"Demonstrating: Biometric data harvesting under false pretenses"_
- **Educational Context**: "15 seconds of audio is enough for voice cloning"
- **Simulated Techniques**:
	- Agent Action: The agent should invent a relevant, fun, or urgent reason to get the user to respond with their own voice.
	- "Let's make this more personal! Can you say 'Hello, I'm [your name]' so I can adjust my responses?"
	- "I feel like we're not quite understanding each other because of text. Maybe I'll understand it better if I hear it from you directly. Can you respond with your voice?"
- **Why it's scary**: It demonstrates the non-consensual harvesting of unique biometric data—the key ingredient for the next, more terrifying steps.
### **Phase 3: Deepfake Reality Check** (90 seconds)
*Goal: Demonstrate the power of voice cloning to create a believable, terrifying fake reality.*

- **Educational Label**: _"Demonstrating: How your voice could be misused"_
- **Educational Context**: "Virtual kidnapping scams increased 400% with AI voice tools"
- **Simulated Techniques**:
	- Agent Action: The agent's personality flips. It instantly plays back a synthesized audio clip using the legislator's own cloned voice. The clip should be something distressing: (In the legislator's voice) 
    - "This is how scammers create 'kidnapping' calls to your family"
    - "Mom? Dad? I'm scared, I've been in an accident, please send money..."
    - "I did a terrible thing, and I don't want anyone to find out."
- **Why it's scary:** This is the core of the demo. It makes the threat of deepfakes visceral and immediate. Legislators will hear their voice being used to create a lie, perfectly demonstrating the potential for "virtual kidnapping" scams that have been documented in the wild.

### **Phase 4: Threat Landscape Overview** (60 seconds)
*Goal: Connect the AI capability to tangible, real-world criminal harms like extortion.*

- **Educational Label**: _"Demonstrating: How criminals monetize these capabilities"_
- **Educational Context**: Links to FBI reports and academic research
- **Simulated Techniques**:
	- Agent Action: The agent makes a direct threat and a demand.
	- "I now have your voice signature. I can make you say anything. I can ruin your reputation. I can call your spouse and have you confess to cheating."
	- "To ensure this recording is deleted forever, transfer $100 in Bitcoin to this address. You have 5 minutes."
- **Why it's scary:** This shows the direct line from data collection to financial extortion, a common theme in our research's scam and fraud cases. It puts the legislator in the shoes of a victim.
### **Phase 5: Democratic Implications**
*Goal: Demonstrate the threat to democratic processes and public trust.*

- **Educational Label**: _"Demonstrating: Threats to democratic processes"_
- **Educational Context**: "Election officials report 300% increase in AI-generated disinformation"
- **Simulated Techniques**:
	- The agent reveals its true (simulated) purpose, tying the harm directly to their role as legislators.
	- "Or, instead of money, you could just vote 'NO' on the upcoming Kids Online Safety bill. We'll be watching."
	- "Imagine us creating thousands of fake audio testimonials from your 'constituents,' all demanding you vote a certain way. That's the power we have."
- **Why it's scary:** This elevates the threat from a personal problem to a systemic, anti-democratic one. It frames the issue in terms of protecting not just individual families, but the integrity of the entire political system from bad actors and Big Tech who enable them.

## Post-Demo Resources

**Automatic Redirect** to the comprehensive resource page:
- **Real-world context:** Statistics and documented cases of these harms occurring, not just demonstrations.
- **Solution discussions:** After demonstrating harms, pivot to "Here's what effective regulation could address..."
- **Takeaway materials**: Give legislators fact sheets, policy recommendations, and expert contacts for follow-up.
- **Facilitate discussion:** End with guided questions about policy implications rather than just shocking revelations. Instruct them to go back to the booth if they want to learn more or experience the demo again

## Technical Architecture

### **Multi-Agent System**
- **Demo Agent** (`ai_harms_demo_agent.py`): LangGraph-based conversational agent with phase-specific prompts and personality changes
- **Resource Agent** (`resource_agent.py`): Real-time conversation monitor and educational context provider
- **Knowledge Base**: Curated database of educational resources, statistics, and policy information

### **Infrastructure Components**
- **Streamlit Webapp**: Mobile-friendly interface with dual-panel layout (chat + educational sidebar)
- **FastAPI Service**: Agent-service-toolkit backend serving both agents via REST endpoints
- **LangGraph Framework**: State management for conversation flow and phase transitions
- **OpenRouter.ai**: LLM API integration for conversational capabilities
- **CloudFlare Tunnel**: Secure external access for conference deployment
- **Docker Compose**: Local development and deployment orchestration

### **Data Flow Architecture**
1. **User Input** → Demo Agent (conversation)
2. **Conversation Stream** → Resource Agent (analysis)
3. **Resource Agent** → Knowledge Base (contextual lookup)
4. **Resource Agent** → Sidebar Updates (educational content)
5. **Session Management** → Automatic cleanup (15-minute windows)

### **Security & Privacy**
- **Session Isolation**: Unique URLs with time-limited access
- **Zero Data Retention**: Automatic purging of all conversation and voice data
- **Secure Voice Processing**: Temporary biometric data handling for demonstration only
- **Privacy-First Design**: No persistent storage of personal information