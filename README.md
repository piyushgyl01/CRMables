# **CRMables CRM Dashboard**

A comprehensive Customer Relationship Management (CRM) system that helps businesses manage leads, track sales pipelines, and analyze performance metrics. Built with a modern React frontend, Express/Node backend, and MongoDB database.

## **Demo Link**
🚀 [Live Demo](https://crmables-frontend.vercel.app/)

## **Quick Start**

### **Clone & Install**
```bash
git clone https://github.com/your-username/crmables-crm.git
cd crmables-crm

# Install backend dependencies
cd server
npm install

# Install frontend dependencies  
cd ../client
npm install
```

### **Environment Setup**
```bash
# Server (.env)
cd server
cp .env.example .env
# Update MONGODB connection string

# Client (.env) 
cd ../client
cp .env.example .env
# Update VITE_API_URL if needed
```

### **Run the Application**
```bash
# Start backend server (from server directory)
npm run dev

# Start frontend client (from client directory) 
npm run dev
```

## **Technologies**

### **Frontend**
- **React 18** - Modern UI library
- **Vite** - Fast build tool and dev server
- **Material-UI (MUI)** - Component library
- **Bootstrap 5** - CSS framework
- **Redux Toolkit** - State management
- **React Router** - Client-side routing
- **Chart.js & Recharts** - Data visualization
- **Axios** - HTTP client

### **Backend**
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **CORS** - Cross-origin resource sharing

### **Deployment**
- **Vercel** - Frontend & backend hosting

## **Demo Video**
📹 Watch a complete walkthrough of CRMables features: [Demo Video Link](https://youtu.be/1rSe-7t55FI)

## **Features**

### **📊 Dashboard**
- Lead overview with key metrics (New, Contacted, Qualified leads)
- Recent leads display with status indicators
- Real-time filtering by lead status
- Clean, responsive card-based layout

### **👥 Lead Management**
- **Create Leads**: Add new prospects with complete details
- **View Leads**: Comprehensive lead listing with filtering
- **Edit Leads**: Update lead information and status
- **Lead Details**: Detailed view with comments and activity
- **Status Tracking**: Monitor lead progression through sales pipeline
- **Priority Management**: Set and sort by priority levels (High, Medium, Low)
- **Time Tracking**: Track expected time to close deals

### **💼 Sales Agent Management**
- Add and manage sales team members
- Assign leads to specific agents
- Agent performance dashboard
- Individual agent lead statistics

### **💬 Comments & Communication**
- Add comments to leads for team collaboration
- Comment history with timestamps
- Author attribution for all comments

### **📈 Reports & Analytics**
- **Lead Status Distribution**: Pie chart showing leads by status
- **Agent Performance**: Bar chart of leads closed by each agent
- **Pipeline Analysis**: Overview of total leads vs closed leads
- Interactive charts with real-time data

### **🔍 Advanced Filtering & Sorting**
- Filter by status, sales agent, and priority
- Sort by priority (High to Low / Low to High)
- Time-to-close range filtering
- Real-time filter application

### **📱 Responsive Design**
- Mobile-first responsive layout
- Touch-friendly interface
- Optimized for all screen sizes

## **API Reference**

### **Leads**
```http
GET    /leads              # Get all leads
POST   /leads              # Create new lead
GET    /lead/:id           # Get lead by ID
PUT    /leads/:id          # Update lead
DELETE /leads/:id          # Delete lead
```

### **Sales Agents**
```http
GET    /salesAgent         # Get all sales agents
POST   /salesAgent         # Create new sales agent
```

### **Comments**
```http
GET    /leads/:id/comments # Get lead comments
POST   /leads/:id/comments # Add comment to lead
```

### **Reports**
```http
GET    /report/last-week   # Get last week's closed leads
GET    /report/pipeline    # Get pipeline statistics
```

### **Sample API Responses**

**GET /leads**
```json
[
  {
    "_id": "64a1b2c3d4e5f6789",
    "name": "John Doe Company",
    "source": "Website",
    "salesAgent": {
      "_id": "64a1b2c3d4e5f6788",
      "name": "Alice Johnson"
    },
    "status": "Qualified",
    "priority": "High",
    "tags": ["enterprise", "urgent"],
    "timeToClose": 30,
    "createdAt": "2024-01-15T10:30:00Z"
  }
]
```

**POST /leads**
```json
{
  "name": "Tech Startup Inc",
  "source": "Referral", 
  "salesAgent": "64a1b2c3d4e5f6788",
  "status": "New",
  "priority": "Medium",
  "tags": ["startup", "tech"],
  "timeToClose": 45
}
```

## **Project Structure**

```
crmables-crm/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── features/       # Feature-specific components
│   │   │   ├── lead/       # Lead management
│   │   │   ├── salesAgent/ # Sales agent features
│   │   │   └── reports/    # Analytics & reports
│   │   ├── hooks/          # Custom React hooks
│   │   ├── app/            # Redux store configuration
│   │   └── main.jsx        # App entry point
│   └── package.json
└── server/                 # Express backend
    ├── models/             # Mongoose schemas
    ├── db/                 # Database connection
    ├── index.js            # Server entry point
    └── package.json
```

## **Contact**

For bugs, feature requests, or collaboration opportunities, please reach out to piyush2022ug@gmail.com

---

**Built with ❤️ by Piyush Goyal**