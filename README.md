# Fame & Dot Discord Bot

**A Node.js Discord bot that brings the classic number-guessing game to your server.**

This project allows two players to challenge each other in a game of "Fame & Dot," where they must guess their opponent's secret 4-digit number with unique digits.

## Key Features
* **Two-Player Gameplay:** Start a game against any user in a Discord channel using slash commands.
* **Secure Setup:** Set your secret number privately using an **ephemeral message**, so only you and the bot know it.
* **Automated Feedback:** Get instant **Fame** and **Dot** feedback after every guess.
* **Turn-Based:** The bot keeps track of whose turn it is, ensuring fair play.
* **Multi-Game Support:** The bot can handle multiple games in different channels or servers simultaneously.

## How to Set Up and Run the Bot

### 1. Prerequisites
* **Node.js** (LTS version recommended) installed on your system.
* A Discord account and a bot token from the [Discord Developer Portal](https://discord.com/developers/applications).

### 2. Installation
Clone the repository:
```bash
git clone https://github.com/your-username/fame-and-dot-bot.git
cd fame-and-dot-bot
```

Install the required Node.js packages:
```bash
npm install
```

### 3. Configuration
Create a `.env` file in the root directory and add your bot token:
```env
DISCORD_TOKEN=YOUR_BOT_TOKEN_HERE
```

Replace `YOUR_BOT_TOKEN_HERE` with the token you obtained from the Discord Developer Portal.

### 4. Running the Bot
From the root directory, run the bot:
```bash
node src/bot.js
```

## Bot Commands

The bot uses modern Discord Slash Commands for a better user experience.

| Command | Description |
| :--- | :--- |
| `/challenge @user` | Starts a new game of Fame & Dot with the mentioned user. |
| `/set_secret [number]` | Privately sets your 4-digit secret number. Digits must be unique. Example: `/set_secret 1234` |
| `/guess [number]` | Makes your guess for the opponent's secret number. Example: `/guess 5678` |
| `/status` | Shows the current game state, including whose turn it is. |
| `/forfeit` | Forfeits the current game and ends the match. |

## Technologies Used
* **Node.js**
* **`discord.js`** - The official library for interacting with the Discord API.
* **`dotenv`** - For securely managing environment variables.
