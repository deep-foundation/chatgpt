# ChatGPT

The ChatGPT package for Deep allows seamless GPT-3.5/GPT-4 integration in your projects, providing AI-powered conversations.

[![npm](https://img.shields.io/npm/v/@deep-foundation/chatgpt.svg)](https://www.npmjs.com/package/@deep-foundation/chatgpt) 
[![Gitpod](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/deep-foundation/chatgpt) 
[![Discord](https://badgen.net/badge/icon/discord?icon=discord&label&color=purple)](https://discord.gg/deep-foundation)

## Guide to Using the ChatGPT Package from Deep Foundation

### 1. Opening Gitpod
- Navigate to [Gitpod](https://gitpod.io/#https://github.com/deep-foundation/dev).
- Wait for the development environment to be fully loaded.

### 2. Opening the Port and Logging in as Admin
- After the Deep server is up and running, open port 3007 by clicking on the link in the Ports tab.
- Open the developer console by pressing F12 and insert the following query to log in as admin and press Enter:
```javascript
const adminId = await deep.id('deep', 'admin');
await deep.login({
  linkId: adminId,
});
```
- Upon successful login, a new interface with links will appear.

### 3. Installing the ChatGPT Package
- Open `Packager` in the DeepCase interface.
- Locate and install the `@deep-foundation/chatgpt` package.

### 4. Granting Admin Rights to All Packages
- Insert the following query into the console to grant admin rights to all packages and press Enter:
```javascript
const joinTypeLinkId = await deep.id("@deep-foundation/core", "Join");
await deep.insert([
  {
    type_id: joinTypeLinkId,
    from_id: await deep.id('deep', 'users', 'packages'),
    to_id: await deep.id('deep', 'admin'),
  },
]);
```

### 5. Inserting the API Key
- Create an `ApiKey` link.
- Open its editor, insert your API key, and save the changes (Ctrl+S).

### 6. Selecting the Model (if needed)
**Note**: By default, the GPT-3.5 `Model` is used. If this is suitable for your needs, you can skip this step.
- To view the available prepared models, right-click on the package link -> space to enter the package space. Here, you can browse through and select the desired model.
- If you want to use another `Model`, note down the ID of your chosen `Model` from the prepared ones. Then, execute the following query, replacing `MODEL` with the ID:
```javascript
const MODEL = '1301'; // Your modelLinkID here

await deep.insert({
  type_id: await deep.id("@deep-foundation/openai", "UsesModel"),
  from_id: await deep.id("@deep-foundation/chatgpt"),
  to_id: MODEL,
  in: {
    type_id: await deep.id("@deep-foundation/core", "Contain"),
    from_id: await deep.id("@deep-foundation/chatgpt"),
  }
});

await deep.insert({
  type_id: await deep.id("@deep-foundation/openai", "UsesModel"),
  from_id: await deep.id('deep', 'admin'),
  to_id: MODEL,
  in: {
    type_id: await deep.id("@deep-foundation/core", "Contain"),
    from_id: await deep.id('deep', 'admin'),
  }
});
```

### 7. Using the ChatGPT Package
- Exit from the package space.
- Create a `Conversation` link specifically from the `@deep-foundation/chatgpt` package.
- Create a `Message` link, open its editor, write your question as the value, and save the changes (Ctrl+S).
- Create a `Reply` link from your `Message` to `Conversation` to send the request.

### 8. Viewing the Answer and Continuing the Dialogue
- To open all messages in the current chat, `Right-click on the Message link from the current Conversation -> traveler -> down -> messagingTree`.
- To continue the dialogue, create a new message with your question and a `Reply` link from your message to the last response from ChatGPT.

### 9. Repeating the Process
- Repeat these steps whenever you want to interact with ChatGPT or create a new dialogue.
