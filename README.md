# Steps for Starting to Use ChatGPT from Deep



Video instruction: https://www.youtube.com/watch?v=ieO2shJyrB8

1. Go to https://github.com/deep-foundation/dev and run Gitpod.
![image](https://user-images.githubusercontent.com/58123600/228636978-0b838aef-43a8-47e1-af20-8ef08911f664.png)

2. Wait for the Deep server to start in the terminal. Once it has started, you will see a message:
![image](https://user-images.githubusercontent.com/58123600/228638401-df7c85da-f5a0-4158-a050-4d6508d3daec.png)
 
3. After the server starts, open the port tab and click on the link to open port 3007.
![image](https://user-images.githubusercontent.com/58123600/228638897-f6373709-ab72-4903-b624-95747d3bff22.png)

4. In the new tab, press f12 to open developer console:
![image](https://user-images.githubusercontent.com/58123600/228978982-b89ab3f8-e22c-47b1-ba58-93b1ee694cab.png)
* And paste following command here and press Enter:
 const adminId = await deep.id('deep', 'admin');
 await deep.login({
  linkId: adminId,
 });
![image](https://user-images.githubusercontent.com/58123600/228979141-e2742a5f-3cd0-4dfe-a094-29c3e9793349.png)
* After clicking the menu on the side, you will see a new interface:
![image](https://user-images.githubusercontent.com/58123600/228640653-5f3cb522-2476-496f-9f18-f40a7abe09a2.png)

5. Insert a query link by right-clicking and holding down the right mouse button.
![image](https://user-images.githubusercontent.com/58123600/228641593-69766ea5-2f89-4e8f-9e3a-a628a9c766b2.png)
![image](https://user-images.githubusercontent.com/58123600/228641719-45fdb877-2430-4872-b431-fe4475834035.png)
![image](https://user-images.githubusercontent.com/58123600/228641728-9d1d948e-cdfc-46e1-80f7-f52e38bf3367.png)

6. Open the editor by right-clicking and holding down the right mouse button on the query link:
![image](https://user-images.githubusercontent.com/58123600/228642069-46c84818-0600-4496-93b3-fa78f3081b2b.png)
* Insert this code: {id:{_gt:922}} and press Ctrl+S to save(if the id of your query connection is not 922, insert its current id instead of 922):
![image](https://user-images.githubusercontent.com/58123600/228642257-551f0a16-ce4d-4fd3-ab4c-3c4d65b251cb.png)

7. Click on the query link, and then click on the next button:
![image](https://user-images.githubusercontent.com/58123600/228642826-15ce35ad-25b1-4a85-8671-46b277e93fd8.png)

<!-- 8. The next step is to open the packager and find the chatgpt package in the "not installed" section:
![image](https://user-images.githubusercontent.com/58123600/228643018-52128c0a-c850-4bea-9ae5-0ca4a59d93be.png)
![image](https://user-images.githubusercontent.com/58123600/228643113-e6a8f64b-bbd9-4409-a6eb-5b3655b6bcd3.png) -->

8. The next step would be to paste the link of the 'PackageQuery'
![image](https://user-images.githubusercontent.com/58123600/230725197-addaf588-3345-46c8-b83c-cc5994b6b8b3.png)

9. Then you need to go to its editor and write the name of the package to be installed, in our case it is: @flakeed/chatgpt and press Ctrs+S:
![image](https://user-images.githubusercontent.com/58123600/230725273-f3999088-5310-4090-9421-edd7e1776680.png)

10. After that we can install the package using install link from npm-packager, creating from user to our PackageQuery with package name
![image](https://user-images.githubusercontent.com/58123600/230725408-864162c0-533b-4c23-90af-ba0783a6a858.png)

11. Click on "promises" to see results of async reactions
![image](https://user-images.githubusercontent.com/58123600/230725530-cf5015d4-bce7-47ac-9b2c-b2554284474b.png)
* ChatGPT package and it dependency Messaging are installed
![image](https://user-images.githubusercontent.com/58123600/230725546-64d5a1d9-c3ea-4eab-ae88-ecc7ca071e34.png)

12. Insert the "Join" link from the chatgpt package to the user:
![image](https://user-images.githubusercontent.com/58123600/228644111-ea9bb52d-bd82-4075-b788-aea1419e8050.png)
![image](https://user-images.githubusercontent.com/58123600/228644352-4da12f75-1cf6-4c74-8726-26b06344bf99.png)

13. Now you can create links to start a chat and chat with ChatGPT:
* First, you need to create an API key for the ChatGPT API by visiting this link: https://platform.openai.com/account/api-keys:
![image](https://user-images.githubusercontent.com/58123600/228636188-df420f07-e112-4395-a260-bb8af2e238f6.png)
Then, copy the API key:
![image](https://user-images.githubusercontent.com/58123600/228636391-f038806c-afd9-456b-904c-d8ad5822d3b0.png)

* Create an OpenAiApiKey link and paste the token from previous step into the editor. Save it by pressing Ctrl+S:
![image](https://user-images.githubusercontent.com/58123600/228644980-d7019a20-ead0-4df8-8a41-433defd47606.png)    
![image](https://user-images.githubusercontent.com/58123600/228645514-76c77927-3a36-48d4-84e2-68486246b199.png)
    
* Create a UsesOpenAiApiKey link to make OpenAiApiKey the current token from user to OpenAiApiKey:
![image](https://user-images.githubusercontent.com/58123600/228646016-9ac76d69-bf7b-471a-84b1-d59bb2771432.png)
    
* Using the UsesModel link:
![image](https://user-images.githubusercontent.com/58123600/230726035-0b7836a7-4c4a-44f0-af19-596f08582389.png)
And select the model that is on the screen:
![image](https://user-images.githubusercontent.com/58123600/230726000-e9b04bb7-bd29-46fc-9c67-e8e63775158c.png)
Creating from the user to the model, or create another model and specify the desired model in the editor, after which you need to create a UsesModel link from the desired Conversation to the model:
![image](https://user-images.githubusercontent.com/58123600/230726099-ea4c79cc-7179-47af-9d84-8b88e0a6faaa.png)
  
* Create a Converstion link:
![image](https://user-images.githubusercontent.com/58123600/228646100-8339f78b-d02f-455a-9e2a-c041b4f43e98.png)

* Create a Message link and enter your question for ChatGPT. Save it by pressing Ctrl+S:
![image](https://user-images.githubusercontent.com/58123600/228646273-c15c36e7-b51d-4242-9e8d-0b8b16c50844.png)
![image](https://user-images.githubusercontent.com/58123600/228646980-fbca8e1f-9feb-4875-822c-166daf8082b6.png)
    
* Create a Reply link from the Message link to the Conversation link:
![image](https://user-images.githubusercontent.com/58123600/228646880-b2ca0873-8177-4661-a22a-776dcdf1eb30.png)
![image](https://user-images.githubusercontent.com/58123600/228647193-f6872bd5-5725-4849-ae1b-72175847c012.png)
![image](https://user-images.githubusercontent.com/58123600/228650984-6fec466d-6b42-4d6f-9411-ee465952cfc0.png)
    
14. To continue chatting with ChatGPT, create a message with a question and then create a reply link from the user message to the ChatGPT message:
![image](https://user-images.githubusercontent.com/58123600/228651204-c9a3b1df-ae55-4e13-8ff0-883b2721a244.png)
![image](https://user-images.githubusercontent.com/58123600/228651669-792f39d0-2327-4e9c-8188-c8eb11ba297e.png)

That's all! You can now continue using ChatGPT by following step 14 as needed.


    





