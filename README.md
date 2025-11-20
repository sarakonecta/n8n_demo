# Tech Learning Path Generator

An n8n workflow that generates personalized learning paths for any technology.

## 🎯 Objective

Complement the CrewAI project (which evaluates technologies) with a system that analyzes **how to learn them**, by querying real resources from GitHub, Dev.to, and StackOverflow.

## 🛠️ Technologies Used

- **n8n** (workflow automation)
- **GitHub API** (repositories and tutorials)
- **Dev.to API** (community articles)
- **StackOverflow API** (frequently asked questions)
- **LiteLLM** (Gemini 2.5 Flash)
- **JavaScript** (data processing)

## 📋 Workflow Structure (10 nodes)

1. **Manual Trigger** - Starts the workflow
2. **Edit Fields** - Input technology to analyze
3. **GitHub API** - Searches for tutorial repositories
4. **Dev.to API** - Searches for articles
5. **StackOverflow API** - Searches for frequently asked questions
6. **Merge** - Combines all data
7. **Code (JavaScript)** - Processes and structures resources
8. **Prepare LLM Request** - Prepares the prompt for Gemini
9. **LiteLLM** - Generates the Learning Path with AI
10. **Edit Fields (Output)** - Formats final result

## 🚀 How to Run

1. Start n8n:
```bash
docker-compose up -d
```

2. Access: http://localhost:5678

3. Open the workflow "Tech Learning Path Generator"

4. Change the technology in the "Edit Fields" node (e.g., `react`, `fastmcp`, `python`)

5. Click "Execute workflow"

## 📊 Output

The workflow generates a structured learning plan with:
- 📊 Summary of available resources
- 📅 Weekly roadmap (Week 1, 2, 3)
- ⭐ Best resources by platform
- ⏱️ Estimated time
- 📈 Difficulty level

## 🔗 Complement with CrewAI

- **CrewAI** → Evaluates the technology (repo health, community, maturity)
- **n8n** → Analyzes how to learn it (resources, plan, timeline)

## 📁 Project Structure
```
n8n_demo/
├── docker-compose.yml          # Docker configuration for n8n
├── README.md                   # This file
└── Tech_Learning_Path_Generator.json  # Exported workflow (backup)
```

## 🎯 Challenge Requirements

✅ n8n installed locally (Docker)
✅ Working workflow with minimum 6 steps (10 nodes implemented)
✅ Functional demonstration ready