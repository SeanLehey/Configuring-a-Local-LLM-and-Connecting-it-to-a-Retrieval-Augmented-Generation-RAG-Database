# Configuring a Local LLM and Connecting it to a Retrieval Augmented Generation (RAG) Database
Creating my GDScript coding companion

## Why Use a RAG?
The data with which Large Language Models (LLMs) are trained is typically outdated by the time the LLM releases, especially when that data is a living, evolving programming language. An update from Godot 4.3 to 4.4 can introduce many changes which may not be accounted for by the data that the LLM was trained on. With a RAG, the LLM can reference the latest documentation and avoid providing inaccurate and out-of-date information.

## Downloading the RAG Database
For this project, our RAG will be Godot's GDScript documentation - specifically, an offline copy. This is available on Godot's website at https://docs.godotengine.org/en/stable/index.html. See below for relevant section:

<img width="1580" height="222" alt="GodotDocumentationDownload" src="https://github.com/user-attachments/assets/d190644a-0feb-4bc3-9688-debec75cbb32" />

Selecting the _Stable_ option downloads a file called _godot-docs-html-stable.zip_. We'll return to this file later.


## Downloading and Configuring LMStudio
