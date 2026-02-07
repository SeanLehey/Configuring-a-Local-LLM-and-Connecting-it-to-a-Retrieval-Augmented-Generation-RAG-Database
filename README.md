# Configuring a Local LLM and Connecting it to a Retrieval Augmented Generation (RAG) Database
Creating my GDScript coding companion

## Hardware Requirements
This is a compute-heavy project which requires a capable GPU. Similar results can be achieved on less powerful systems via quantization and other methods, but I recommend you use the latest GPU you can afford. My laptop for this project has the following specifications:

Intel Core Ultra 9 275HX Processor
Nvidia GeForce RTX 5090 24GB (Mobile version, which is roughly equivalent to a desktop 4070/4080)
64GB DDR5 RAM
2TB SSD

## Why Use a RAG?
The data with which Large Language Models (LLMs) are trained is typically outdated by the time the LLM releases, especially when that data is a living, evolving programming language. An update from Godot 4.3 to 4.4 can introduce many changes which may not be accounted for by the data that the LLM was trained on. With a RAG, the LLM can reference the latest documentation and avoid providing inaccurate and out-of-date information.

## Downloading the RAG Database
For this project, our RAG will be Godot's GDScript documentation - specifically, an offline copy. This is available on Godot's website at https://docs.godotengine.org/en/stable/index.html. See below for relevant section:

<img width="1580" height="222" alt="GodotDocumentationDownload" src="https://github.com/user-attachments/assets/d190644a-0feb-4bc3-9688-debec75cbb32" />

Selecting the _Stable_ option downloads a file called _godot-docs-html-stable.zip_. We'll return to this file later.


## Downloading and Configuring LMStudio

For this project, we'll be deploying our LLM using LMStudio. This is an open-source project which allows users to download a variety of models to use locally on their system. Simply download the appropriate client for your operating system from LMStudio's [website](https://lmstudio.ai/).

### Model Selection
On the left side of your LMStudio client, select _Model Search_ and download your desired model. For our project, we'll be downloading GPT-OSS 20B. 

<img width="734" height="118" alt="LMStudioModelChoice" src="https://github.com/user-attachments/assets/efa4e5c1-2d34-48c8-bf53-f7877c3631b2" />

