<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00AEEF,100:7F00FF&height=200&section=header&text=Welcome%20to%20My%20Profile&fontSize=45&fontColor=ffffff&animation=fadeIn">
</p>

# 😳Hi cutey, I'm what
I am a Discord Bot Developer & Full‑Stack Learner  
I build interactive Discord systems, experiment with infrastructure, and love exploring new tech.

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?size=24&duration=4000&color=00AEEF&center=true&vCenter=true&width=500&lines=What+The+Twink+Developer;Hehe+Hi+Sexy+Beast" />
</p>

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

## 🌱 I know I am Just so Amazing
You are so welcome for that example *mwah.
Feel free to follow me maybe, of course only if you want to. 

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

## 👾My Discord
`_c0raz0n`
> Although I probably won't friend you lol, sorry.

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">

## 😘 Common issues
> For discord bots. I know I'm so helpful

*note all code examples are in java script.

<details>
  <summary>Click to open this section</summary>
  
### 🔄 Commands Running Twice

Cause: Duplicate event listeners or multiple bot instances.
Fix:

Ensure client.login() is only called once.

Remove duplicate imports or handlers.

Stop old bot processes on your host.

<details>
<summary><strong>Show code example</strong></summary>

```js
// Avoid double listeners
client.once('ready', () => {
    console.log('Bot online!');
});
```
<details>
</details>

<div style="border-left: 4px solid #4A90E2; padding-left: 12px; margin: 20px 0;">


### 🌐 API Requests Failing
<details>
Cause: Missing headers, rate limits, or incorrect endpoint.
Fix:

Add required headers (e.g., Content-Type: application/json).

Log response status to detect rate limits.

Verify the API URL and parameters.

<details>
<summary><strong>Show code example</strong></summary>

```js
// Basic fetch with headers
const response = await fetch('https://api.example.com/data', {
    method: 'GET',
    headers: { 'Content-Type': 'application/json' }
});
```
<details>

### 🆕 Newer Modal Components Not Working

Cause: Newer modal components (Label Components, Radio Groups, Select Menus inside modals) require strict layout rules.
Fix:

You must use modal.addLabelComponents() instead of modal.addComponents().

Radio Groups: Max 10 options.

Select Menus: Max 25 options.

Select menus must be wrapped in a Label Component.

Text Display Blocks (Type 10) are non-interactive.

<details>
<summary><strong>Show code example</strong></summary>

```js
// Newer modal components example (Discord.js v14.23+)
const {
    ModalBuilder,
    ActionRowBuilder,
    TextInputBuilder,
    TextInputStyle,
    StringSelectMenuBuilder,
    StringSelectMenuOptionBuilder
} = require('discord.js');

const modal = new ModalBuilder()
    .setCustomId('settingsModal')
    .setTitle('Bot Settings');

// Text input
const input = new TextInputBuilder()
    .setCustomId('username')
    .setLabel('Enter your username')
    .setStyle(TextInputStyle.Short);

// Select menu (must be wrapped)
const select = new StringSelectMenuBuilder()
    .setCustomId('themeSelect')
    .setPlaceholder('Choose a theme')
    .addOptions(
        new StringSelectMenuOptionBuilder().setLabel('Dark').setValue('dark'),
        new StringSelectMenuOptionBuilder().setLabel('Light').setValue('light')
    );

// Correct layout
modal.addLabelComponents(
    new ActionRowBuilder().addComponents(input),
    new ActionRowBuilder().addComponents(select)
);
```
</details>
</details>
