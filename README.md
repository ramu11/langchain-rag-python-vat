# langchain-rag-python-video-audio-transcription

Components
InstructLab
InstructLab is used specifically for model alignment in our project. It employs a method called Large-scale Alignment for chatBots (LAB), which enhances LLMs using far less human-generated information and fewer computing resources than typical retraining methods. InstructLab’s approach includes taxonomy-driven data curation, large-scale synthetic data generation, and iterative, large-scale alignment tuning. This allows us to improve our model’s alignment efficiently, making it more suitable for specific contexts and use cases of providing stock recommendations.

Podman AI Lab
Podman AI Lab serves as our local environment for working with Large Language Models. Podman AI Lab provides by default a recipe catalog with common AI use cases, a curated set of open source models, and a playground for learning, prototyping, and experimentation. In our case, we use Podman AI Lab to serve our InstructLab merlinite-7b-lab model locally, ensuring data privacy and security. This approach also allows us to quickly get started with AI in our application without depending on infrastructure beyond our laptop.

LangChain
LangChain is the backbone of our natural language processing (NLP) pipeline, including the creation of summarisation and recommendation chains. It offers a flexible and powerful framework for building language model applications, allowing us to easily create complex NLP chains essential for our AI agent to process financial reports and generate recommendations. LangChain’s modular nature facilitates easier alignment and adjustment of the AI’s behaviour. Its comprehensive toolkit for agent creation allows us to define the agent’s behaviour, decision-making process, and interaction with other components.

We also leverage LangChain for building the agent custom evaluator. For evaluation, LangChain’s flexible prompt templates and output parsers enable us to create a robust system for assessing the AI’s performance and alignment with our model guidelines including safety requirements.

Prerequisites
Before we begin, ensure you have the following installed on your system:

Python 3.11 or higher
pip (Python package installer)
git

Step 1: Set Up InstructLab
InstructLab is used for model alignment in our project. To set it up:

Follow the installation instructions in the Getting Started section of the InstructLab README in GitHub to set up the environment and dependencies.
Make sure you download the merlinite-7b-lab model, which is an InstructLab-enhanced version of the Mistral model.

Step 2: Set Up Podman AI Lab
Podman AI Lab serves as our local environment for working with Small Language Models.

Install Podman Desktop from the official website: https://podman-desktop.io/
Install the Podman AI Lab extension within Podman Desktop. For this, open Podman Desktop, navigate to the Extensions section and install the “Podman AI Lab” extension.
Use Podman AI Lab to serve the InstructLab merlinite-7b-lab model locally:
Open Podman AI Lab within Podman Desktop
Navigate to the Models section
Import the merlinite-7b-lab model you downloaded in Step 1, via its GGUF file.

Start a model service for merlinite-7b-lab. This can be easily achieved by creating a playground (which will create and start a service) which also allows you to test the working condition of your model by chatting via its endpoint.
Finally look at the services details as you need the server endpoint to configure the agent.





