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
