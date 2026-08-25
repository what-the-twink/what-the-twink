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
### 🧠 How it works
User runs /createpanel

Bot shows a modal

User types text

Bot creates a new channel named after the user

Bot sends an embed inside that channel

Embed title = username

Embed description = modal text
