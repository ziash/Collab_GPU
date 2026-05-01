# Collab_GPU
Use Google Collab for free GPU access

---------------------------------------------------------------------------
Install and run xterm with following commands:
----------
1. Goto Google Colab and Create a New Notebook.
2. In the upper right corner -> Click down arrow and change runtime type to "TPU" from "CPU". Click save.
3. Connect.
<img width="1222" height="705" alt="image" src="https://github.com/user-attachments/assets/cf3f3fbb-465e-4d2b-8fe5-3bcb5bef1a01" />

Once GPU is connected; we need to install XTERM. This is used to run ollama in the background (and not on our main notebook interface).
Use below 3 commands to do that.

!pip install colab-xterm

%load_ext colabxterm

%xterm

Once this is done you will see XTERM started as below screenshot
<img width="1222" height="705" alt="image" src="https://github.com/user-attachments/assets/d73480cd-bb29-4378-af9c-bbfa30453c69" />


In the new Terminal Run Following Commands (not in notebook/ in terminal)
-------------
apt install screen
apt install zstd

How to go inside screen and get out of it
-------------
To go inside screen type: screen
To get outside type: CTRL A + CTRL D
Reconnect to same screen again: screen -r (reconnect)


Inside screen, run following commands:
-------------
curl -fsSL https://ollama.com/install.sh | sh
ollama serve

Outside screen, on main terminal, run following command:
--------------
// Since the GPU RAM is 15GB useable; I will choose a model almost half a billion in parameters to run smoother.
I choose gemma4:latest.
You can also pull
ollama pull qwen3.5:9b
ollama run qwen3.5:9b --verbose
