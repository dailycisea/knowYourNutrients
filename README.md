# knowYourNutrients

## Building MiniProject for Analysis and Nutrition Search using Llama-3.2-80B-Vision-Instruct-Turbo and tavily <br/>
A. Prerequisites
-	Python
-	Anaconda
-	Gradio
-	Prompt engineering<br/>

B. Step by step
1.	Create Virtual Environment using conda
```
conda create --name agent python=3.10.14
conda activate agent
```
2.	Install required libraries <br/>
requirement.txt
```
#python 3.10.14
numpy==1.26.4
together==1.2.0
python-dotenv~=1.0.1
tiktoken==0.7.0
blobfile==3.0.0
torch==2.4.0
matplotlib==3.9.2
wolframalpha==5.1.3
tavily-python==0.5.0
llama-stack==0.0.36
llama-stack-client==0.0.35
gradio==4.43.0
```

3.	How to get api
- together.ai <br/>
we're not gonna using local llama 3.2 but we'll using Inference from together.ai to run our model <br/>
Step : <br/>
First, access https://www.together.ai/ <br/>
login using your account<br/>
Click `Dashboard`<br/>
Get your api key<br/>
![image](https://github.com/user-attachments/assets/301e0b11-4bd4-4031-9f29-51923b1931ba)
-	tavily
Step : <br/>
access https://tavily.com/ <br/>
Login using your account <br/>
For free account, you can get 1000 request API limit <br/>
![image](https://github.com/user-attachments/assets/1c2bca45-f299-4c64-9dac-8359ccfaeb2c)

Create .env file
```
TOGETHER_API_KEY=xxx
TAVILY_API_KEY=tvly-xxx
```
4.	Prompt Engineering <br/>
We will use `https://smith.langchain.com/hub/hardkothari/prompt-maker` to create our prompt <br/>
-	Define task<br/>
food detection given image inside of refrigerator
-	Buat prompt singkat<br/>
You are professional nutritionist and food expert, What food ingredients are in the refrigerator? 
-	Detailkan dengan template prompt <br/>
```
system

You are an expert Prompt Writer for Large Language Models.

human

Your goal is to improve the prompt given below for {task} :

--------------------

Prompt: {lazy_prompt}

--------------------

Here are several tips on writing great prompts:

-------

Start the prompt by stating that it is an expert in the subject.

Put instructions at the beginning of the prompt and use ### or to separate the instruction and context 

Be specific, descriptive and as detailed as possible about the desired context, outcome, length, format, style, etc 

---------

Here's an example of a great prompt:

As a master YouTube content creator, develop an engaging script that revolves around the theme of "Exploring Ancient Ruins."
Your script should encompass exciting discoveries, historical insights, and a sense of adventure.
Include a mix of on-screen narration, engaging visuals, and possibly interactions with co-hosts or experts.
The script should ideally result in a video of around 10-15 minutes, providing viewers with a captivating journey through the secrets of the past.

Example:
"Welcome back, fellow history enthusiasts, to our channel! Today, we embark on a thrilling expedition..."
-----


Now, improve the prompt.

IMPROVED PROMPT:
```
Send it to openAI chatgpt<br/>
Here the result <br/>
![image](https://github.com/user-attachments/assets/fecb8c4f-b1ce-4522-bd35-cfe63f10281a)<br/>

5.	Buat function untuk llama 3.2 vision dan fungsi pendukung
6.	Buat gradio untuk deployment <br/>
Complete source code<br/>
https://github.com/dailycisea/knowYourNutrients
Reference
https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/
https://learn.deeplearning.ai/courses/introducing-multimodal-llama-3-2/lesson/1/introduction
https://smith.langchain.com/hub/hardkothari/prompt-maker
https://www.youtube.com/watch?v=MUZtVEDKXsk&t=618s


