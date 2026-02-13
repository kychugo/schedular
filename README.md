# 🤖 AI Schedule Generator

An intelligent scheduling platform that automatically generates personalized timetables based on your todo list, availability, and fixed commitments.

## ✨ Features

- **Smart Auto-Scheduling**: Automatically allocates flexible tasks into your available time slots
- **Fixed Time Slots**: Lock specific activities (e.g., "6pm-7pm dinner") that cannot be moved
- **Unavailable Periods**: Block out times when you're busy or unavailable
- **Flexible Tasks**: Add tasks with estimated durations that can be scheduled flexibly
- **Multi-Day Planning**: Generate schedules across multiple days
- **Export Options**: Download your schedule as Markdown (.md) or DOCX format
- **User-Friendly Interface**: Intuitive design with clear visual feedback
- **Mobile Responsive**: Works on desktop, tablet, and mobile devices
- **No Installation Required**: Single HTML file - just open and use!

## 🚀 Getting Started

### Quick Start

1. Download or clone this repository
2. Open `index.html` in any modern web browser
3. Start creating your schedule!

### How to Use

1. **Set Working Hours**: Define your available time range (e.g., 9:00 AM - 6:00 PM)
2. **Select Date Range**: Choose start and end dates for your schedule
3. **Add Todo Items**: Enter flexible tasks with estimated durations
4. **Add Fixed Times**: Set activities with specific time requirements (cannot be moved)
5. **Mark Unavailable Times**: Block periods when you're not available
6. **Generate Schedule**: Click "Generate Schedule" to create your timetable
7. **Export**: Download your schedule as Markdown or DOCX

## 📋 Example Usage

### Scenario
You need to:
- Complete a 2-hour project report (flexible timing)
- Have dinner at 6pm-7pm (fixed time)
- Attend a team meeting at 2pm-3pm (unavailable/blocked)

The AI scheduler will:
1. Lock dinner at 6pm-7pm (cannot be moved)
2. Block 2pm-3pm for the meeting (unavailable)
3. Find the best 2-hour slot for your project report
4. Generate a complete weekly schedule respecting all constraints

## 🎯 Key Capabilities

### Constraint Handling
- **Hard Constraints**: Fixed times and unavailable periods are never modified
- **Smart Allocation**: Flexible tasks are optimally placed in available slots
- **Conflict Prevention**: Automatically prevents scheduling conflicts
- **Overflow Handling**: Warns when tasks cannot fit within available time

### Export Formats
- **Markdown**: Clean, readable tables perfect for documentation
- **DOCX**: Professional Word documents ready for sharing

## 🛠️ Technical Details

- **Technology**: Pure HTML5, CSS3, and JavaScript
- **Dependencies**: docx.js (for DOCX export), FileSaver.js (for file downloads)
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **No Backend Required**: Runs entirely client-side

## 📸 Screenshots

![AI Schedule Generator Interface](https://github.com/user-attachments/assets/f7b389cc-3653-45f0-ade4-284e31fbf930)

![Generated Schedule Example](https://github.com/user-attachments/assets/507b6f24-2a48-4d09-b86e-933bcea5de4d)

## 🎨 Features Breakdown

### Input Configuration Panel
- **Working Hours**: Set daily start/end times
- **Todo Items (Flexible)**: Tasks that can be scheduled anywhere
- **Fixed Time Items**: Activities locked to specific times
- **Unavailable Times**: Blocked periods for meetings, breaks, etc.

### Generated Schedule Panel
- **Visual Timeline**: Color-coded schedule by task type
  - 🔵 Blue: Flexible tasks
  - 🟡 Yellow: Fixed time items
  - 🔴 Red: Unavailable/blocked periods
- **Multi-Day View**: See your entire week at a glance
- **Export Options**: Download in your preferred format

## 📝 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Feel free to fork, modify, and improve this scheduler. Contributions are welcome!

## 🐛 Known Limitations

- DOCX export requires CDN access (may be blocked in restricted environments)
- Time slots are calculated in hours (not minutes)
- Single timezone support

## 💡 Future Enhancements

- Priority-based task scheduling
- Break time automation
- Calendar integration (Google Calendar, Outlook)
- Task dependencies
- Recurring tasks support
- Dark mode theme