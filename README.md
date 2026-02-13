# 🤖 AI Schedule Generator

An intelligent scheduling platform that automatically generates personalized timetables based on your todo list, availability, and fixed commitments. Enhanced with AI integration, priority-based scheduling, automatic breaks, task dependencies, and recurring tasks support.

## ✨ Core Features

### Smart Scheduling
- **Priority-Based Scheduling**: Assign High/Medium/Low priority to tasks - high-priority tasks are scheduled first
- **Task Dependencies**: Set prerequisites for tasks - dependent tasks automatically schedule after their dependencies
- **Recurring Tasks**: Support for daily and weekly recurring tasks that auto-generate across your date range
- **Break Time Automation**: Automatically insert breaks after specified work duration (e.g., 15 min break every 2 hours)
- **Fixed Time Slots**: Lock specific activities (e.g., "12pm-1pm lunch") that cannot be moved
- **Blocked Periods**: Mark times when you're unavailable for scheduling

### AI Integration
- **AI-Powered Suggestions**: Connect to Pollinations.ai API for intelligent scheduling recommendations
- **Model Selection**: Choose from multiple AI models (OpenAI, Claude, Gemini, etc.)
- **Manual API Key Entry**: Securely store your API key in browser localStorage
- **Smart Optimization**: AI analyzes your tasks and suggests optimal scheduling strategies

### User Experience
- **Dark Mode**: Toggle between light and dark themes with preference persistence
- **Visual Priority Indicators**: Color-coded tasks (Red=High, Yellow=Medium, Blue=Low, Green=Breaks)
- **Dependency Visualization**: Clear badges showing task dependencies
- **Recurrence Badges**: Visual indicators for daily/weekly recurring tasks
- **Export Options**: Download schedules as Markdown (.md) or DOCX format
- **Mobile Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **No Installation Required**: Single HTML file - just open and use!

## 🚀 Getting Started

### Quick Start

1. Download or clone this repository
2. Open `index.html` in any modern web browser
3. (Optional) Add your Pollinations.ai API key for AI features
4. Start creating your schedule!

## 📖 How to Use

### 1. Configure Your Schedule

#### Set Working Hours
- Define your daily available time range (e.g., 9:00 AM - 5:00 PM)
- Select start and end dates for your schedule

#### Configure Break Times
- Set break duration (default: 15 minutes)
- Set break frequency (default: every 2 hours)
- Breaks are automatically inserted after accumulated work time

### 2. Add Tasks

#### Flexible Tasks (with Priority & Dependencies)
- **Task Name**: What needs to be done
- **Duration**: Estimated hours needed
- **Priority**: High/Medium/Low (high-priority tasks scheduled first)
- **Recurrence**: None/Daily/Weekly for repeating tasks
- **Dependencies**: Select prerequisite tasks that must complete first

#### Fixed Time Blocks
- Activities that must occur at specific times
- Example: "Lunch 12:00-13:00" cannot be moved

#### Blocked Times
- Periods when you're unavailable
- Example: "Team Meeting 14:00-15:00"

### 3. AI Settings (Optional)

1. Click "🤖 AI Settings" to expand the panel
2. Enter your Pollinations.ai API key ([Get one here](https://enter.pollinations.ai))
3. Click "🔄 Refresh" to load available models
4. Select your preferred AI model
5. Click "✨ AI Suggest" to get intelligent scheduling recommendations

⚠️ **Security Note**: API keys are stored in browser localStorage and are vulnerable to XSS attacks. Use with caution.

### 4. Generate & Export

- Click "Generate Schedule" to create your timetable
- Review the color-coded schedule with:
  - 🔴 High Priority tasks
  - 🟡 Medium Priority / Fixed blocks
  - 🔵 Low Priority tasks
  - 🟢 Automatic breaks
  - 🔴 Blocked times
- Export to Markdown or DOCX format
- Toggle dark mode with the theme button

## 📋 Example Usage

### Scenario
You need to:
- Review code changes (2 hours, HIGH priority)
- Write documentation (1.5 hours, MEDIUM priority, depends on code review)
- Have lunch at 12:00-13:00 (fixed time)
- Take 15-minute breaks every 2 hours

### Result
The AI scheduler will:
1. **Schedule high-priority first**: Review code changes at 9:00-11:00
2. **Insert automatic break**: 15-min break at 11:00-11:15
3. **Respect fixed times**: Lunch locked at 12:00-13:00
4. **Handle dependencies**: Write documentation scheduled after code review (13:00-14:30)
5. **Apply recurrence**: If daily recurrence set, documentation repeats on subsequent days
6. **Prevent conflicts**: Automatically avoids scheduling conflicts

## 🎯 Key Capabilities

### Intelligent Constraint Handling
- **Hard Constraints**: Fixed times and blocked periods are never modified
- **Priority Ordering**: High-priority tasks always scheduled before lower priorities
- **Dependency Resolution**: Tasks automatically ordered based on prerequisites
- **Circular Dependency Detection**: Warns when dependencies form a cycle
- **Smart Allocation**: Flexible tasks optimally placed in available slots
- **Break Insertion**: Automatic breaks based on accumulated work time
- **Recurrence Expansion**: Daily/weekly tasks automatically generated across date range

### AI-Powered Optimization
- **Model Flexibility**: Choose from multiple AI providers
- **Context-Aware Suggestions**: AI considers all your constraints
- **Intelligent Recommendations**: Get suggestions for task ordering and timing
- **API Integration**: Direct connection to Pollinations.ai services

## 🛠️ Technical Details

- **Technology**: Pure HTML5, CSS3, and JavaScript (ES6+)
- **Dependencies**: 
  - docx.js v7.8.2 (for DOCX export)
  - FileSaver.js v2.0.5 (for file downloads)
- **AI Integration**: Pollinations.ai API (https://gen.pollinations.ai)
  - GET /text/models - Fetch available AI models
  - POST /v1/chat/completions - Get AI scheduling suggestions
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Storage**: localStorage for API keys and theme preferences
- **No Backend Required**: Runs entirely client-side

## 🎨 Features Breakdown

### Configuration Panel
- **Working Hours**: Set daily start/end times
- **Date Range**: Define scheduling period
- **Break Settings**: Configure automatic break insertion
- **Flexible Tasks**: Priority, duration, recurrence, dependencies
- **Fixed Time Blocks**: Activities locked to specific times
- **Blocked Times**: Unavailable periods for meetings, etc.
- **AI Settings**: API key and model selection (collapsible)

### Generated Schedule Panel
- **Visual Timeline**: Color-coded schedule by type
  - 🔴 Red border: High priority tasks
  - 🟡 Yellow: Medium priority / Fixed blocks
  - 🔵 Blue: Low priority tasks
  - 🟢 Green: Automatic breaks
  - 🔴 Red: Blocked/unavailable times
- **Priority Badges**: HIGH / MEDIUM / LOW labels
- **Recurrence Indicators**: Daily / Weekly badges
- **Dependency Labels**: Shows prerequisite relationships
- **Multi-Day View**: See your entire schedule at a glance
- **Export Buttons**: Generate Markdown or DOCX files

## 📸 Screenshots

### Light Mode
![Enhanced AI Scheduler Interface](https://github.com/user-attachments/assets/69c66ae1-867f-476b-9489-38889b62bf37)

### Dark Mode
![Dark Mode Theme](https://github.com/user-attachments/assets/62fd1d53-66c4-4350-b464-bca95260a92c)

### Generated Schedule with All Features
![Complete Schedule Example](https://github.com/user-attachments/assets/3e69a13a-04dd-4514-8340-9f79937b7f07)

*Shows priority-based scheduling, automatic breaks, task dependencies, recurring tasks, and fixed time blocks*

## 📝 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Feel free to fork, modify, and improve this scheduler. Contributions are welcome!

## 🐛 Known Limitations

- DOCX export requires CDN access (may be blocked in restricted environments)
- AI features require internet connection and valid API key
- API keys stored in localStorage are vulnerable to XSS attacks
- Time calculations in hours (0.5 hour increments supported)
- Single timezone support
- Circular dependencies detected but not auto-resolved

## 💡 Future Enhancements

- ~~Priority-based task scheduling~~ ✅ **Implemented**
- ~~Break time automation~~ ✅ **Implemented**
- ~~Task dependencies~~ ✅ **Implemented**
- ~~Recurring tasks support~~ ✅ **Implemented**
- ~~Dark mode theme~~ ✅ **Implemented**
- ~~AI integration for smart scheduling~~ ✅ **Implemented**
- Calendar integration (Google Calendar, Outlook) - Planned
- Drag-and-drop task rearrangement - Planned
- Task categories and tagging - Planned
- Time zone support - Planned
- Offline mode with service workers - Planned

## 🔒 Security Considerations

### API Key Storage
- API keys are stored in browser's localStorage
- Vulnerable to XSS attacks and accessible by any script
- **Recommendation**: Use publishable keys only, never production secret keys
- Consider using environment-specific keys for testing

### Best Practices
- Clear localStorage when using shared computers
- Don't commit API keys to version control
- Use separate keys for development and production
- Regularly rotate API keys
- Monitor API usage for unusual activity