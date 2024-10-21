# knowYourNutrients
Outline
A. Prerequisites
-	Python
-	Anaconda
-	Gradio
-	Prompt engineering
B. Step by step
1.	Create Virtual Environment using conda
```
conda create --name agent python= 3.10.14
conda activate agent
```
2.	Install required libraries
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
-	https://www.together.ai/
-	https://tavily.com/
4.	Prompt Engineering
-	Define purpose
-	Buat prompt singkat
-	Detailkan dengan template prompt
5.	Buat function untuk llama 3.2 vision dan fungsi pendukung
6.	Buat gradio untuk deployment
Complete source code 
https://github.com/dailycisea/knowYourNutrients
Reference
https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/
https://learn.deeplearning.ai/courses/introducing-multimodal-llama-3-2/lesson/1/introduction
https://smith.langchain.com/hub/hardkothari/prompt-maker
https://www.youtube.com/watch?v=MUZtVEDKXsk&t=618s


