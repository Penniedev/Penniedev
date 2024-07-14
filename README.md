
# Pennie Discord Bot

Welcome to my Discord bot! This bot is designed to enhance your server experience with various features.

## Prerequisites

Before getting started, make sure you have the following:

- ![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white) Node.js and npm (or yarn) installed on your system
- ![Discord](https://img.shields.io/badge/-Discord-5865F2?style=flat-square&logo=discord&logoColor=white) Discord account with permissions to create bots and manage servers
- ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) MongoDB (or another database of your choice) for storing bot data

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Penniedev/new-v2
   cd new-v2
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

   or if you prefer yarn:

   ```bash
   yarn install
   ```

3. **Set up environment variables**

   Copy the `.env.sample` file to `.env` in the root directory:

   ```bash
   cp .env.sample .env
   ```

   Update the `.env` file with your actual values:

   ```env
   TOKEN=your_discord_bot_token
   MongoURI=your_mongodb_connection_uri
   TestServers=["your_test_server_id_1","your_test_server_id_2"]
   Developers=["your_discord_user_id"]
   ```

   Replace `your_discord_bot_token`, `your_mongodb_connection_uri`, `your_test_server_id_1`, `your_test_server_id_2`, and `your_discord_user_id` with your actual values.

4. **Start the bot**

   ```bash
   npm start
   ```

   or

   ```bash
   yarn start
   ```

## 🛠️ Slash Command Template

Use this template for creating new slash commands in your bot. You can copy and paste it into your project's template folder for easy access.

```javascript
const { ApplicationCommandOptionType } = require("discord.js");
const { SlashCommand } = require("gbfcommands");

module.exports = class SlashCommandTemplate extends SlashCommand {
  constructor(client) {
    super(client, {
      name: "",
      description: "",
      UserPermissions: [],
      BotPermissions: [],
      category: "",
      cooldown: 5,
      options: [
        {
          name: "",
          description: "",
          type: ApplicationCommandOptionType.String,
        },
      ],
      async execute({ client, interaction }) {},
    });
  }
};
```

Replace the placeholders (`name`, `description`, etc.) with appropriate values for each slash command you create.

## 📄 License

This project is licensed under the **Private Use License** and signed by

[![Signature](https://iili.io/dBcVeRV.md.png)](https://freeimage.host/i/dBcVeRV) 

```error
ERROR: You are not permitted to use this code, in part or in whole, for any purpose other than private personal use. Any unauthorized use, reproduction, or distribution is strictly prohibited.
```
