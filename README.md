[![npm](https://img.shields.io/npm/v/@deep-foundation/chatgpt.svg)](https://www.npmjs.com/package/@deep-foundation/chatgpt) 
[![Gitpod](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/deep-foundation/dev) 
[![Discord](https://badgen.net/badge/icon/discord?icon=discord&label&color=purple)](https://discord.gg/deep-foundation)

# Steps for Starting to Use ChatGPT from Deep



Video instruction: https://www.youtube.com/watch?v=63oAjA536AE

1. Go to https://github.com/deep-foundation/dev and run Gitpod.
![image](https://user-images.githubusercontent.com/58123600/228636978-0b838aef-43a8-47e1-af20-8ef08911f664.png)

2. Wait for the Deep server to start in the terminal. Once it has started, you will see a message:
![image](https://user-images.githubusercontent.com/58123600/228638401-df7c85da-f5a0-4158-a050-4d6508d3daec.png)
 
3. After the server starts, open the port tab and click on the link to open port 3007.
![image](https://user-images.githubusercontent.com/58123600/228638897-f6373709-ab72-4903-b624-95747d3bff22.png)

4. In the new tab, press f12 to open developer console:
![image](https://user-images.githubusercontent.com/58123600/230727268-3c3e04d4-caca-40cc-8aba-9feba6c20672.png)
* And paste following command here and press Enter:
 const adminId = await deep.id('deep', 'admin');
 await deep.login({
  linkId: adminId,
 });
![image](https://user-images.githubusercontent.com/58123600/230727312-98da474c-a84d-4b79-9b61-af02d7443cdf.png)
* After clicking the menu on the side, you will see a new interface:
![image](https://user-images.githubusercontent.com/58123600/230727327-6296a9cf-089d-465e-a6ac-e9e1091bdeb8.png)

5. Insert a query link by right-clicking and holding down the right mouse button.
![image](https://user-images.githubusercontent.com/58123600/230727395-56c7be3e-8b3a-49be-80df-d2b44d41ff28.png)
![image](https://user-images.githubusercontent.com/58123600/230727446-7d6cd1f8-beb5-4136-b8d7-35ea852b7738.png)

6. Open the editor by right-clicking and holding down the right mouse button on the query link:
![image](https://user-images.githubusercontent.com/58123600/230727482-ba1bcc24-48af-4043-a87a-557dbe38d06c.png)
* Insert this code: {id:{_gt:942}} and press Ctrl+S to save(if the id of your query connection is not 942, insert its current id instead of 942):
![image](https://user-images.githubusercontent.com/58123600/230727530-340b545a-f1c5-435c-8549-19afd99ec853.png)

7. Click on the query link, and then click on the next button:
![image](https://user-images.githubusercontent.com/58123600/230727581-3663d465-6ec5-44bb-8de7-11935411d092.png)

<!-- 8. The next step is to open the packager and find the chatgpt package in the "not installed" section:
![image](https://user-images.githubusercontent.com/58123600/228643018-52128c0a-c850-4bea-9ae5-0ca4a59d93be.png)
![image](https://user-images.githubusercontent.com/58123600/228643113-e6a8f64b-bbd9-4409-a6eb-5b3655b6bcd3.png) -->

8. The next step would be to paste the link of the 'PackageQuery'
![image](https://user-images.githubusercontent.com/58123600/230727623-610fd438-bea8-4d2c-bb88-a1cfe34aec30.png)

9. Then you need to go to its editor and write the name of the package to be installed, in our case it is: @flakeed/chatgpt and press Ctrs+S:
![image](https://user-images.githubusercontent.com/58123600/230727643-3cd76a84-a250-45aa-9d65-6aab18df329a.png)

10. After that we can install the package using install link from npm-packager, creating from user to our PackageQuery with package name
![image](https://user-images.githubusercontent.com/58123600/230727677-1e375892-e0b9-49af-bd97-31cfb66d6c5f.png)
![image](https://user-images.githubusercontent.com/58123600/230727717-4b840fd3-a03e-4f91-9932-d7b2b6edd4d3.png)

11. Click on "promises" to see results of async reactions
![image](https://user-images.githubusercontent.com/58123600/230727949-b35d5432-f15a-4548-9453-ad525d3d8227.png)
* ChatGPT package and it dependency Messaging are installed
![image](https://user-images.githubusercontent.com/58123600/230727965-46d901e2-22b1-43c4-96eb-3e99ca9d11f4.png)

12. Insert the "Join" link from the chatgpt package to the user:
![image](https://user-images.githubusercontent.com/58123600/230728023-08853cd1-4304-4c95-9bf9-0c9384b160c0.png)
![image](https://user-images.githubusercontent.com/58123600/230728028-c36de826-a3ad-4a22-9ad9-f60a4d42f4e4.png)

13. Now you can create links to start a chat and chat with ChatGPT:
* First, you need to create an API key for the ChatGPT API by visiting this link: https://platform.openai.com/account/api-keys:
![image](https://user-images.githubusercontent.com/58123600/228636188-df420f07-e112-4395-a260-bb8af2e238f6.png)
Then, copy the API key:
![image](https://user-images.githubusercontent.com/58123600/228636391-f038806c-afd9-456b-904c-d8ad5822d3b0.png)

* Create an OpenAiApiKey link and paste the token from previous step into the editor. Save it by pressing Ctrl+S:
![image](https://user-images.githubusercontent.com/58123600/230728071-03108fdc-2932-4c16-bb5a-bcee38431172.png)   
![image](https://user-images.githubusercontent.com/58123600/230728120-e46b18b8-25fe-42bd-baf0-c25a8d1a396d.png)
    
* Create a UsesOpenAiApiKey link to make OpenAiApiKey the current token from user to OpenAiApiKey(if you have one link "OpenAiApiKey" then you can skip this step, it is used automatically):
![image](https://user-images.githubusercontent.com/58123600/230728181-a5614da1-e03c-4606-be06-9b9b64d6b122.png)
![image](https://user-images.githubusercontent.com/58123600/230728237-978ee823-7fb5-4f78-ad77-d84cbdf7b286.png)
    
* Using the UsesModel link(if you are satisfied with the default gpt-3.5-turbo model you can skip this step):
![image](https://user-images.githubusercontent.com/58123600/230728267-7d31b8e8-23f0-466a-8bd9-5460af962732.png)
And select the model that is on the screen:
![image](https://user-images.githubusercontent.com/58123600/230728288-ae2e9cd7-1533-4812-8524-20e4a0733d30.png)
Creating from the user to the model, or create another model and specify the desired model in the editor, after which you need to create a UsesModel link from the desired Conversation to the model:
![image](https://user-images.githubusercontent.com/58123600/230728427-43385679-9eb9-433e-97c0-360228205e15.png)
  
* Create a Converstion link:
![image](https://user-images.githubusercontent.com/58123600/230728467-572ffd1f-d623-4970-b43a-add47f1e6f13.png)

* Create a Message link and enter your question for ChatGPT. Save it by pressing Ctrl+S:
![image](https://user-images.githubusercontent.com/58123600/230728506-ba65ba31-b590-43ea-b7d9-9cdee1fa158d.png)
![image](https://user-images.githubusercontent.com/58123600/230728539-e8d64daf-6cd9-4da1-be49-b5c7143a5444.png)
    
* Create a Reply link from the Message link to the Conversation link:
![image](https://user-images.githubusercontent.com/58123600/230728581-04fa2b59-7ae3-4cd7-80ad-ce5b408b9147.png)
![image](https://user-images.githubusercontent.com/58123600/230728614-7049a7cd-ca6e-4d9c-9ce1-f7632514359a.png)
After that you can see the response from ChatGPT
![image](https://user-images.githubusercontent.com/58123600/230728690-24dab2cd-1c49-4d4d-ab56-8a31a5010071.png)
    
14. To continue chatting with ChatGPT, create a Message link again and in its editor ask your question and press Ctrl+S, then create a Reply Link from the user's message you just created to the ChatGPT response from the previous request:
![image](https://user-images.githubusercontent.com/58123600/230728943-a83cc6e9-6176-469b-ba2b-25577d99ba04.png)
![image](https://user-images.githubusercontent.com/58123600/230728972-305bb848-3f16-4174-ade2-7594140699c6.png)
After that we get another response from the bot:
![image](https://user-images.githubusercontent.com/58123600/230729086-0e01b8c7-81f1-497e-8d76-1ddf47fe6073.png)

That's all! You can now continue using ChatGPT by following step 14 as needed.


    





