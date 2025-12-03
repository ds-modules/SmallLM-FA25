# SmallLM-FA25
Another Iteration of Small Models Demo - for Jupytercon 2025
Small Language Models via GPT4All and OpenAI API

This work is based on work from Greg Merritt - [Ollama Demo](https://github.com/ds-modules/ollama-demo) which was based on work from Pamela Fox [Ollama Python Playground](https://github.com/pamelafox/ollama-python-playground). The OpenAI notebook is based on one from Jedidia Tsang for Data 6 [Proeject Part 2](https://github.com/data-6-berkeley/materials-fa24/blob/main/proj/project-part2.ipynb)

I am not an expert in the field and the speed these things are changing this material and even the approach will be soon obsolete. But it was my objective to illustrate in some small and incremental way what is going on with these models which are changing out lives and disrupting our society every day. I taught these in the last week of my class [Data Science for Economists](https://www.econ148.org/) so these students had 1) already seen quite a bit of Python programming, and 2) I motivated the discussion around the cost of models and the cost of tokens eg elemental economics of language models.   

Basically the notebooks can also be understood as introducing three Python AI oriented packages: `GPT4all` is a package which facilitates the use of open source models in a Pythonic framework, `llama-cpp-python` provides more direct Python bindings to the llama.cpp inference engine, and `openai` is a Python framework for interacting with OpenAI models via an API. The models can be stored and hosted locally.

## Notebooks 
 - [HuggingFace_Hub_Download_gguf.ipynb](HuggingFace_Hub_Download_gguf.ipynb) - **NEW!** Download GGUF models directly from Hugging Face Hub to a shared directory. This is the recommended approach for downloading models, as it provides access to thousands of models and allows configuring a shared cache directory for classroom use. Works with llama-cpp-python for testing.
 
 - [GPT4All_Download_gguf.ipynb](GPT4All_Download_gguf.ipynb) - only open this notebook if you need to download the models - this notebook has code for both local storage or on an online server.  An instructor would want to use a notebook like this to set up the framework for instruction.
   
 - [GPT4All_SmallLM_Demo.ipynb](GPT4All_SmallLM_Demo.ipynb) - this is the main demonstration notebook - and assumes that the instructor has already put the models in a shared repository 

 - [LlamaCpp_SmallLM_Demo.ipynb](LlamaCpp_SmallLM_Demo.ipynb) - **NEW!** An alternative to the GPT4All demo that uses the `llama-cpp-python` package instead. This notebook provides more direct access to the llama.cpp inference engine, with detailed explanations of the package, its features, and how it compares to GPT4All. Works with any GGUF model from Hugging Face.
   
 - [Inside_Small_Model.ipynb](Inside_Small_Model.ipynb) - **NEW!** An educational deep-dive into how language models work internally. This notebook visualizes tokenization, model output probabilities, and decoding strategies (temperature, top-k, top-p). Works with any .gguf model (OLMo, Mistral, Phi, Qwen, Llama, etc.) and requires no PyTorch - just GPT4All. Perfect for teaching students what happens "inside" a small model.
   
 - [OpenAI_API.ipynb](OpenAI_API.ipynb) - this notebook uses a python package from Open AI and an API to connect to OpenAI models. It requires that the instructor purchase an API key and that instructor have a way to circulate the key to the students.
   
 - [Anthropic_API.ipynb](Anthropic_API.ipynb) - use Anthropic pandas library and API key instead of OpenAI.


## There a few key issues for setup
- **model weights** In the Small Models notebook - the small models "weights" must be downloaded from Huggingface. I include here a [separate notebook](GPT4All_Download_gguf.ipynb) for this. When I taught this in class I did this step myself, then put the models into a shared directory on the Juptyerhub where I was teaching and where the students could read them from.
- **which models?** I was going for the smallest of models. Partly to fit on the parameters of the teaching Jupyterhub at UC Berkeley where students had 4gb ram and no GPU. But that is precisely what I was trying to teach: what can a tiny model do. So specifically I used models around 1 GB - which means 1b parameters and quantized.
- **Using an API** In the OpenAI API Notebook *you need an API key*. I opened an acccount and put $50 down and after 150 students had used the API we had used $0.05 = 5 cents worth of API access.  For this demo I am using the shared directory to share API key access only to authenticated users

##  Link to Run on Cal-ICOR hub - November 2025 [Interact Link](https://jupyter.cal-icor.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fds-modules%2FSmallLM-FA25&urlpath=lab%2Ftree%2FSmallLM-FA25%2F)
