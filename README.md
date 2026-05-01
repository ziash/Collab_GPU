# Collab_GPU
Use Google Collab for free GPU access

---------------------------------------------------------------------------
Install and run xterm with following commands:
----------
1. Goto Google Colab and Create a New Notebook.
2. In the upper right corner -> Click down arrow and change runtime type to "TPU" from "CPU". Click save.
3. Connect.
<img width="1222" height="705" alt="image" src="https://github.com/user-attachments/assets/cf3f3fbb-465e-4d2b-8fe5-3bcb5bef1a01" />

!pip install colab-xterm

%load_ext colabxterm

%xterm

In the Terminal Run Following Commands:
-------------
apt install screen
apt install zstd

Inside screen, run following commands:
-------------
curl -fsSL https://ollama.com/install.sh | sh
ollama serve

Outside screen, on main terminal, run following command:
--------------
ollama pull qwen3.5:9b
ollama run qwen3.5:9b --verbose
