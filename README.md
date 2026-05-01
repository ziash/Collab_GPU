# Collab_GPU
Use Google Collab for free GPU access

---------------------------------------------------------------------------
Install and run xterm with following commands:
----------
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
