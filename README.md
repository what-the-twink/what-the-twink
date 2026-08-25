# 👋 Hey, I’m what!
I am a Discord Bot Developer & Full‑Stack Learner  
I build interactive Discord systems, experiment with infrastructure, and love exploring new tech.

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

  ## 🚀 What I Do
**Discord Bot Development**
Full‑stack learning — JS/TS, APIs, backend systems

Infrastructure tinkering — hosting, automation, self‑hosting

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

  ## 🌐 Projects I Work On
Developer focused on interaction systems, automation, and scalable bot features.
I also work on repositories designed for new developers to help them build bots, structure projects, and understand core backend concepts.

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

## 😘 Code Example Just For You

<details>
  <summary>Click to open this section</summary>
  
```js
const {
  SlashCommandBuilder,
  ModalBuilder,
  TextInputBuilder,
  TextInputStyle,
  ActionRowBuilder,
  ChannelType,
  EmbedBuilder
} = require('discord.js');

module.exports = {
  data: new SlashCommandBuilder()
    .setName('createpanel')
    .setDescription('Opens a modal and creates a channel with the submitted text'),

  async execute(interaction) {

    // Create the modal
    const modal = new ModalBuilder()
      .setCustomId('panelModal')
      .setTitle('Create a Panel');

    // Create the text input
    const input = new TextInputBuilder()
      .setCustomId('panelText')
      .setLabel('Enter the panel text')
      .setStyle(TextInputStyle.Paragraph);

    // Add input to modal
    const row = new ActionRowBuilder().addComponents(input);
    modal.addComponents(row);

    // Show modal
    await interaction.showModal(modal);
  }
};
```

```js
module.exports = {
  async execute(interaction) {

    // Check if it's the modal
    if (interaction.isModalSubmit() && interaction.customId === 'panelModal') {

      // Get the text input
      const text = interaction.fields.getTextInputValue('panelText');

      // Create a new channel
      const channel = await interaction.guild.channels.create({
        name: `panel-${interaction.user.username}`,
        type: ChannelType.GuildText
      });

      // Build the embed
      const embed = new EmbedBuilder()
        .setTitle(interaction.user.username)
        .setDescription(text)
        .setColor('Blue')
        .setTimestamp();

      // Send embed in the new channel
      await channel.send({ embeds: [embed] });

      // Acknowledge the modal submission
      await interaction.reply({
        content: `Your panel has been created in ${channel}!`,
        ephemeral: true
      });
    }
  }
};
```
</details>

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">
  
### 🧠 How it works
User runs /createpanel

Bot shows a modal

User types text

Bot creates a new channel named after the user

Bot sends an embed inside that channel

Embed title = username

Embed description = modal text

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

## 🌱 I know I am Just so Amazing
You are so welcome for that example *mwah.
Feel free to follow me maybe, of course only if you want to. 

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

## ✌️My Badges
Totally not fake 👀😙
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=fff)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=fff)
![Discord.js](https://img.shields.io/badge/Discord.js-5865F2?style=for-the-badge&logo=discord&logoColor=fff)
![Express](https://img.shields.io/badge/Express-000?style=for-the-badge&logo=express&logoColor=fff)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=fff)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=fff)
![VS Code](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=fff)
![Discord Bots](https://img.shields.io/badge/Discord_Bot_Developer-5865F2?style=for-the-badge&logo=discord&logoColor=fff)
![Slash Commands](https://img.shields.io/badge/Slash_Commands-000?style=for-the-badge&logo=slashdot&logoColor=fff)
![Modals](https://img.shields.io/badge/Modals-1E90FF?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=fff)
![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=fff)
![Website](https://img.shields.io/badge/Website-1E90FF?style=for-the-badge&logo=googlechrome&logoColor=fff)
