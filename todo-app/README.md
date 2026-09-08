# To-Do List Application

A modern, feature-rich to-do list application with local storage functionality. Built with vanilla JavaScript, HTML5, and CSS3.

## 🌟 Features

### Core Functionality
- ✅ **Add Tasks** - Create new to-do items with ease
- ✅ **Mark Complete** - Check off tasks as you complete them
- ✅ **Edit Tasks** - Modify existing task text
- ✅ **Delete Tasks** - Remove tasks with confirmation dialog
- ✅ **Local Storage** - All tasks automatically saved to browser storage and persist across sessions
- ✅ **Filter Tasks** - View All, Active, or Completed tasks
- ✅ **Clear Completed** - Remove all completed tasks at once
- ✅ **Task Statistics** - See total and completed task counts in real-time

### User Experience
- 🎨 **Modern Design** - Beautiful gradient interface with smooth animations
- 📱 **Fully Responsive** - Works perfectly on desktop, tablet, and mobile devices
- ⚡ **Fast & Lightweight** - No dependencies, pure vanilla JavaScript
- 🔒 **Secure** - XSS protection with HTML sanitization
- ♿ **Accessible** - Keyboard navigation support (Enter to add task)

## 📁 Files

```
todo-app/
├── index.html       # Application structure and HTML markup
├── styles.css       # Beautiful styling with animations
├── script.js        # Full JavaScript functionality
└── README.md        # This file
```

## 🚀 How to Use

### Quick Start
1. **Download or clone** this folder
2. **Open `index.html`** in your web browser
3. **Start adding tasks!**

### Adding Tasks
- Type your task in the input field
- Click the "Add Task" button OR press Enter
- Tasks are automatically saved to local storage

### Managing Tasks
- **Check box** - Mark task as complete/incomplete
- **Edit button** - Modify the task text
- **Delete button** - Remove the task (with confirmation)

### Filtering Tasks
- Click **All** to see all tasks
- Click **Active** to see incomplete tasks only
- Click **Completed** to see finished tasks only

### Clearing Tasks
- Click **Clear Completed** to remove all finished tasks
- The button is disabled if there are no completed tasks

## 💾 Local Storage

Your tasks are automatically stored in your browser's local storage:
- **Storage Key**: `todoAppTasks`
- **Persistence**: Data remains even after closing the browser
- **Auto-save**: Changes save instantly with every action

To clear all saved data, open browser DevTools (F12) and run:
```javascript
localStorage.removeItem('todoAppTasks');
location.reload();
```

## 🎨 Design Features

### Visual Design
- **Gradient Background**: Purple to violet gradient for an elegant look
- **Card-based Layout**: Clean white card on gradient background
- **Color Scheme**:
  - Primary: #667eea (Blue-purple)
  - Secondary: #764ba2 (Deep purple)
  - Accents: Green (edit), Red (delete), Orange (clear)

### Animations
- **Slide-in Effect**: Main card slides in smoothly on load
- **Item Transitions**: Tasks appear and disappear smoothly
- **Hover Effects**: Buttons and items respond to user interaction
- **Smooth Scrolling**: Custom scrollbar for task list

### Responsive Breakpoints
- **Desktop**: Full layout with side-by-side elements
- **Tablet**: Optimized spacing and touch targets
- **Mobile**: Stacked layout with full-width buttons

## 🔧 Technical Details

### Technologies Used
- **HTML5** - Semantic markup
- **CSS3** - Gradients, animations, flexbox
- **Vanilla JavaScript (ES6)** - No frameworks or libraries

### Browser Compatibility
- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- IE 11: ⚠️ Partial support (no animations)

### Class Structure

The application uses an Object-Oriented approach with a single `TodoApp` class:

```javascript
class TodoApp {
    constructor()      // Initialize app
    init()            // Setup
    attachEventListeners() // Bind events
    addTodo()         // Create new task
    deleteTodo()      // Remove task
    toggleTodo()      // Mark complete
    editTodo()        // Modify task
    clearCompleted()  // Remove finished tasks
    getFilteredTodos() // Filter tasks
    updateStats()     // Update counters
    render()          // Update DOM
    saveToStorage()   // Save to localStorage
    loadFromStorage() // Load from localStorage
    escapeHtml()      // XSS protection
}
```

## 🎯 Usage Examples

### Example: Add Multiple Tasks
```
1. Type: "Buy groceries" → Enter
2. Type: "Call dentist" → Enter
3. Type: "Finish project" → Enter
4. View all tasks in the list
```

### Example: Manage Tasks
```
1. Check "Buy groceries" to mark as complete
2. Click Edit on "Call dentist" to change it
3. Click Delete on a task to remove it
4. Click "Clear Completed" to clean up
```

### Example: Filter and Track
```
1. Click "Active" to see pending tasks
2. Click "Completed" to review finished tasks
3. View statistics at the bottom
4. Click "All" to see everything
```

## 🔒 Security Features

- **XSS Protection**: Text is sanitized using `textContent` and `innerHTML` with escaped content
- **Input Validation**: 
  - Empty input check
  - Maximum length validation (200 characters)
  - Trimming whitespace
- **User Confirmations**: Delete and clear operations require confirmation

## 📊 Data Structure

Each task is stored as an object:
```javascript
{
    id: 1694184301000,              // Unique timestamp ID
    text: "Buy groceries",          // Task text
    completed: false,               // Completion status
    createdAt: "9/8/2026, 8:01:30" // Creation timestamp
}
```

All tasks are stored in an array in localStorage as JSON.

## 🎓 Learning Resources

This project demonstrates:
- **DOM Manipulation** - Create, update, and remove elements
- **Event Handling** - Click, keypress, change events
- **Local Storage API** - Save and retrieve data
- **CSS Animations** - Smooth transitions and effects
- **Object-Oriented JavaScript** - Class-based design
- **ES6 Features** - Arrow functions, template literals, etc.

## 💡 Future Enhancement Ideas

Consider adding:
- Task priority levels (High, Medium, Low)
- Due dates and reminders
- Task categories or tags
- Search/filter by keyword
- Dark mode toggle
- Drag-and-drop reordering
- Data export (CSV, JSON)
- Cloud synchronization

## 📝 License

This project is free to use and modify for personal and educational purposes.

## 🤝 Contributing

Feel free to fork, modify, and improve this project. Some ideas:
- Add more features
- Improve styling
- Optimize performance
- Add tests
- Create a mobile app version

## 📧 Support

For questions or issues, feel free to open an issue on GitHub.

---

**Happy organizing! 🎯📋**
