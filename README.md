# Lead Qualification Assistant

A sophisticated AI-powered lead qualification system that helps businesses identify high-quality prospects through intelligent conversational flows. Built with React, TypeScript, and integrated with Make.com for automated lead processing.

## 🌟 Features

- **Intelligent Conversation Flow**: Guided 3-step qualification process
- **Real-time Lead Scoring**: Automatic qualification based on company size, problem definition, and budget
- **Make.com Integration**: Seamless webhook integration for automated lead processing
- **Beautiful UI/UX**: Modern gradient design with smooth animations and micro-interactions
- **Progress Tracking**: Visual progress indicators and step-by-step guidance
- **Error Handling**: Comprehensive error handling with user-friendly messages
- **Responsive Design**: Optimized for all device sizes
- **Real-time Status**: Live connection status and processing indicators

## 🚀 Live Demo

Visit the live application: [https://beautiful-moxie-7d4b25.netlify.app](https://beautiful-moxie-7d4b25.netlify.app)

## 🛠️ Tech Stack

- **Frontend**: React 18, TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Build Tool**: Vite
- **Deployment**: Netlify
- **Automation**: Make.com (formerly Integromat)

## 📋 Prerequisites

- Node.js 18+ 
- npm or yarn
- Make.com account (for webhook integration)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/lead-qualification-assistant.git
   cd lead-qualification-assistant
Install dependencies


npm install
Start the development server


npm run dev
Open your browser
Navigate to http://localhost:5173

⚙️ Configuration
Make.com Webhook Setup
Create a new scenario in Make.com
Add a webhook trigger
Copy the webhook URL
Update the MAKE_WEBHOOK_URL constant in src/App.tsx:

const MAKE_WEBHOOK_URL = 'your-make-webhook-url-here';
Lead Qualification Logic
The system automatically qualifies leads based on:

Company Size: Enterprise indicators (500+ employees)
Problem Definition: Clear use cases with business impact
Budget & Timeline: Defined budget and implementation timeline
📊 Data Flow
User Interaction: Prospect answers 3 qualification questions
Lead Scoring: Algorithm evaluates responses for qualification
Webhook Transmission: Lead data sent to Make.com scenario
Automated Processing: Make.com handles lead routing and follow-up
🎨 Design Features
Apple-level Aesthetics: Clean, sophisticated visual design
Gradient Backgrounds: Modern purple-to-slate gradient theme
Micro-interactions: Hover states, transitions, and animations
Progress Visualization: Real-time progress tracking
Status Indicators: Connection status and processing feedback
Responsive Layout: Mobile-first design approach
📁 Project Structure

src/
├── App.tsx              # Main application component
├── main.tsx            # Application entry point
├── index.css           # Global styles and Tailwind imports
└── vite-env.d.ts       # TypeScript environment definitions

public/
└── vite.svg            # Vite logo

config/
├── tailwind.config.js  # Tailwind CSS configuration
├── postcss.config.js   # PostCSS configuration
├── vite.config.ts      # Vite build configuration
└── tsconfig.json       # TypeScript configuration
🔄 Qualification Process
Step 1: Company Size
Captures company scale and enterprise indicators
Options: 1-10, 11-50, 51-200, 500+ employees
Step 2: Problem Definition
Identifies specific business challenges
Looks for efficiency, automation, scaling needs
Step 3: Budget & Timeline
Assesses financial readiness and urgency
Evaluates implementation timeline
Step 4: Qualification Result
Automatic lead scoring and classification
Immediate feedback to prospect
Data transmission to Make.com
📈 Lead Scoring Algorithm

const classifyLead = (data: QualificationData): boolean => {
  // Enterprise indicators
  const isEnterprise = companySize.includes('500+') || 
                      companySize.includes('large') || 
                      companySize.includes('enterprise');

  // Clear use case indicators
  const hasClearUseCase = problem.length > 50 && 
                         (problem.includes('efficiency') || 
                          problem.includes('automation') || 
                          problem.includes('scale'));

  // Budget indicators
  const hasBudget = budgetTimeline.includes('$') || 
                   budgetTimeline.includes('budget') || 
                   budgetTimeline.includes('approved');

  return isEnterprise || (hasClearUseCase && hasBudget);
};
🚀 Deployment
Netlify (Recommended)
Build the project


npm run build
Deploy to Netlify

Connect your GitHub repository to Netlify
Set build command: npm run build
Set publish directory: dist
Manual Deployment
Build for production


npm run build
Deploy the dist folder to your hosting provider

🔧 Available Scripts
npm run dev - Start development server
npm run build - Build for production
npm run preview - Preview production build
npm run lint - Run ESLint
🌐 Environment Variables
No environment variables required for basic functionality. The Make.com webhook URL is configured directly in the code.

🤝 Contributing
Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

🆘 Support
If you encounter any issues or have questions:

Check the Issues page
Create a new issue with detailed information
Include browser console errors if applicable
🙏 Acknowledgments
Built with Vite for lightning-fast development
Styled with Tailwind CSS for utility-first styling
Icons provided by Lucide React
Automated workflows powered by Make.com
📊 Analytics & Tracking
The application includes comprehensive error tracking and webhook status monitoring to ensure reliable lead data transmission to your Make.com scenarios.

Made with ❤️ for better lead qualification
