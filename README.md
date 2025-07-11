# 🧙‍♂️ Fantasy Adventure Game Master Agent

A text-based **fantasy adventure game** built with **OpenAI Agents SDK**, where players explore a magical world, make decisions, battle monsters, and earn loot — all powered by smart agents.

## 🎯 Project Overview

This is an interactive CLI game where the narrative unfolds dynamically based on player input and AI decisions. The system uses:

- 🧠 **Agents** (Narrator, Monster, Item) for different game roles  
- 🛠️ **Tools** for randomness and event generation  
- 🔁 **Agent Handoff** to switch context during gameplay  
- 🧑‍💻 **User Choices** to influence outcomes  
- 🎮 **Short-form adventures** (2–3 events + ending)

## 🗂️ Folder Structure

```

fantasy-game/
├── main.py
├── .env
├── requirements.txt
│
├── agents/
│   ├── base\_agent.py
│   ├── narrator\_agent.py
│   ├── monster\_agent.py
│   └── item\_agent.py
│
├── tools/
│   ├── dice\_tools.py
│   └── event\_tools.py
│
└── utils/
└── game\_utils.py

````

## 💡 How It Works

### 🔹 Agents
| Agent          | Role                                             |
|----------------|--------------------------------------------------|
| **NarratorAgent** | Describes story scenes, presents choices        |
| **MonsterAgent**  | Handles combat logic using dice rolls           |
| **ItemAgent**     | Gives loot rewards or heals the player          |

### 🔹 Tools
- `roll_dice(sides)` – simulates dice roll (used for randomness)
- `generate_random_event(location)` – generates a contextual event

### 🔹 Agent Handoff Flow
1. Narrator sets the scene
2. User picks an action
3. MonsterAgent handles combat if needed
4. ItemAgent provides rewards
5. Game ends after 2–3 turns

## ⚙️ Setup Instructions

### 1. Clone the Project

```bash
git clone https://github.com/yourusername/fantasy-game-master-agent.git
cd fantasy-game-master-agent
````

### 2. Create Virtual Environment

```bash
python -m venv venv
# Activate it
venv\Scripts\activate   # Windows
source venv/bin/activate  # macOS/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Key

Create a `.env` file and add:

```
OPENROUTER_API_KEY=your_openrouter_api_key_here
OPENROUTER_BASE_URL=https://openrouter.ai/api/v1
```

## 🚀 Run the Game

```bash
python main.py
```

## 🎮 Example Gameplay

```
🎮 Welcome to the Fantasy Adventure Game!
This is a text-based adventure powered by AI agents.

Enter your character's name: Aria

🌟 Welcome, Aria! Your adventure begins...

🎮 Starting Fantasy Adventure Game...
🎮 Game Master Agent System Active...

🧍 Player: Aria (Level 1)
📍 Location: forest
❤️ Health: 100/100
💰 Gold: 50, 🌟 XP: 0

📘 Story: As you walk into the dense forest, a goblin suddenly jumps out from behind a tree.
📘 Choices: ['Fight the goblin', 'Try to sneak past', 'Use magic']

What will you do? fight

⚔️ A monster appears!
You roll: 17 | Monster rolls: 14
✅ You defeated the monster!
🎁 Loot: You found a Magic Ring!
```

## ✅ Features

* 🗡️ Turn-based battles using dice rolls
* 🧭 Narrative generated dynamically via Claude-3 model
* 🧠 AI agents handle specific tasks and switch seamlessly
* 💬 Player input impacts story direction
* 📦 Loot rewards, XP, and gold system
* 🎬 Game ends after a few events (not endless)

## 🧩 Technologies Used

* [OpenAI Agent SDK](https://platform.openai.com/docs/assistants/overview)
* [OpenRouter API](https://openrouter.ai/)
* `openai`, `python-dotenv`
* Python 3.8+
