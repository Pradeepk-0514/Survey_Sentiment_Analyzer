#  Survey Sentiment Analyzer

An AI-powered web application for analyzing survey feedback, identifying sentiment and key issues, assessing urgency and attrition risk, and generating actionable recommendations using Claude AI.

##  Overview

**Survey Sentiment Analyzer** transforms open-ended survey responses into meaningful insights using AI.

The application provides an interactive dashboard where users can:

* Analyze individual survey responses
* Detect positive, neutral, or negative sentiment
* Identify important issues and themes
* Calculate confidence scores
* Assess urgency and attrition risk
* View department-level sentiment
* Analyze organizational trends
* Generate role-specific action plans
* Visualize sentiment trends using charts

The application is designed as a lightweight **HR and employee-feedback intelligence dashboard**.

---

##  Features

###  Overview Dashboard

The dashboard provides a high-level view of survey feedback, including:

* Total responses
* Average sentiment
* High-urgency responses
* Pending actions
* Sentiment by department
* Top emerging issues
* Six-month sentiment distribution

The sentiment trend is visualized using **Chart.js**.

###  Individual Response Analysis

Users can paste an open-ended survey response and analyze it with Claude AI.

The analyzer generates:

* Sentiment
* Confidence score
* Summary
* Key issues
* Urgency level
* Urgency reason
* Attrition risk
* Flagged dimensions
* Role-specific action nudges

The AI response is requested in a structured JSON format, which is then displayed in the dashboard.

###  Batch Insights

The Batch Insights section provides organization-level analysis using department data.

It includes:

* Department
* Number of responses
* Sentiment score
* Top issue
* Sentiment trend

Users can also ask Claude questions about organizational trends.

###  Action Nudges

The application generates role-specific action plans based on:

* Department
* Responsible role
* Detected issue

Each generated recommendation includes:

* Priority
* Recommended action
* Timeline
* Expected outcome

This helps convert survey insights into practical organizational actions.

---

##  Technologies Used

| Technology    | Purpose                               |
| ------------- | ------------------------------------- |
| HTML5         | Application structure                 |
| CSS3          | Responsive UI and styling             |
| JavaScript    | Application logic                     |
| Chart.js      | Data visualization                    |
| Claude AI     | Sentiment and organizational analysis |
| Anthropic API | AI service integration                |

Chart.js is loaded through a CDN in the application.

---

##  Project Structure

```text
survey-sentiment-analyzer/
│
├── index.html
├── README.md
├── LICENSE
└── assets/
    └── screenshots/
```

> If your actual file has a different name, such as `survey.html`, rename `index.html` in this structure accordingly.

---

##  How It Works

```text
User enters survey response
            │
            ▼
     Survey Analyzer
            │
            ▼
       Claude AI API
            │
            ▼
   Structured AI Response
            │
     ┌──────┼─────────┐
     ▼      ▼         ▼
 Sentiment Issues   Risk
     │      │         │
     └──────┼─────────┘
            ▼
     Action Recommendations
            │
            ▼
       Dashboard UI
```

---

## AI Analysis

The application sends the survey response along with contextual information such as:

* Department
* Survey type
* Respondent role

Claude is instructed to return structured information containing sentiment, confidence, summary, issues, urgency, attrition risk, dimensions, and recommended actions.

---

##  Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Pradeepk-0514/survey-sentiment-analyzer.git
```

### 2. Open the project

```bash
cd survey-sentiment-analyzer
```

### 3. Run the application

Since the current project is a frontend HTML/CSS/JavaScript application, you can open the HTML file in a browser.

For a better development experience, use a local development server such as VS Code Live Server.

### 4. Configure Claude API

The application currently sends requests to the Anthropic Messages API.

Before using the AI features, configure the required API authentication appropriately.

>  **Security:** Do not expose a real Anthropic API key directly inside frontend JavaScript or commit it to GitHub. For production use, route API requests through a backend/serverless endpoint and store the key in environment variables.

---

##  Example Use Case

### Employee Feedback

**Input:**

```text
The workload has increased significantly and I haven't had a
career development discussion with my manager for several months.
I enjoy the work but feel that my efforts are not recognized.
```

### AI Analysis

The system can identify:

```text
Sentiment: Negative
Urgency: High
Attrition Risk: High

Potential Issues:
- Workload
- Career development
- Recognition

Recommended Actions:
- Schedule a manager check-in
- Review workload
- Discuss career development
- Improve employee recognition
```

---

##  Dashboard Sections

| Section          | Purpose                               |
| ---------------- | ------------------------------------- |
| Overview         | Organization-level sentiment overview |
| Analyze Response | Individual survey analysis            |
| Batch Insights   | Department-level analysis             |
| Action Nudges    | Recommended organizational actions    |

---

##  UI Design

The application uses a clean, minimal dashboard interface with:

* Responsive layout
* Card-based components
* Sentiment badges
* Department progress bars
* Interactive tabs
* Data visualization
* Loading indicators
* Mobile-friendly layout

The interface includes responsive breakpoints for smaller screens.

---

##  Future Enhancements

Potential improvements include:

* CSV/Excel survey upload
* Bulk survey analysis
* Historical response database
* User authentication
* Admin dashboard
* Advanced sentiment trends
* Word-cloud visualization
* Export reports as PDF
* Email notifications
* Department comparison
* Real-time analytics
* Secure backend API
* Database integration
* AI-generated executive reports

---

##  Security Considerations

The current prototype communicates with the Anthropic API directly from client-side JavaScript.

For a production deployment:

1. Create a backend API.
2. Store the Anthropic API key in environment variables.
3. Never expose API credentials in frontend source code.
4. Validate user input on the server.
5. Add authentication and authorization.
6. Implement rate limiting.
7. Avoid storing sensitive employee information unnecessarily.

---

##  Author

**Pradeep K**

GitHub: `https://github.com/Pradeepk-0514`

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

**Built with HTML, CSS, JavaScript, Chart.js and Claude AI.**
