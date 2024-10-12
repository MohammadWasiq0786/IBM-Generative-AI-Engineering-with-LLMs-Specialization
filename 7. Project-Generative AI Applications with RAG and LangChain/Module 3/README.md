# Termina Commands

#### Virtual Environment

```bash
pip install virtualenv 
virtualenv my_env # create a virtual environment named my_env
source my_env/bin/activate # activate my_env
```

#### Libraries Installation 
```bash
# installing necessary pacakges in my_env
python3.11 -m pip install \
gradio==4.44.0 \
ibm-watsonx-ai==1.1.2  \
langchain==0.2.11 \
langchain-community==0.2.10 \
langchain-ibm==0.1.11 \
chromadb==0.4.24 \
pypdf==4.3.1 \
pydantic==2.9.1
```

#### Run the App
```bash
python qabot.py
```

# Module Summary: Create a QA Bot to Read Your Document

Congratulations! You have completed this module. At this point in the course, you know: 

* Gradio is an open-source Python library for creating customizable web-based user interfaces
* To set it up:
  * Write the Python code
  * Create the Gradio interface
  * Launch the Gradio server using the launch method
  * Access the web interface through a local or public URL provided by Gradio
* To code a simple text input and output with the Gradio interface, use the gr.Interface function
* To upload or drop files with Gradio, use gr.File
