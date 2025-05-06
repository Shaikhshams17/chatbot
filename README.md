
To get started, first clone this repo:

$ git clone 

$ cd gpt2bot
Create and activate an environment (optional):

# Using conda
$ conda create -n gpt2bot python=3.7.6
$ conda activate gpt2bot

# Using venv (make sure your Python is 3.6+)
$ python3 -m venv venv
$ source venv/bin/activate  # Unix
$ venv\Scripts\activate  # Windows
Install the requirements:

$ pip install -r requirements.txt
Copy a config (see available configs):

cp configs/medium-cpu.cfg my_chatbot.cfg
Set your parameters such as API token in the config:

$ nano my_chatbot.cfg
Run the chatbot:

$ python run_bot.py --type=telegram --config=my_chatbot.cfg
3. Start chatting!


Just start texting. Append "@gif" for the bot to also generate a GIF. To reset, type "/start".

How to improve?
If you feel like your bot is a bit off, you would need to fine-tune its parameters to match your conversational style (small talk, fact questions, philosophy - all require different parameters). Go to your configuration file and slightly change the parameters of the generator. The fastest way to assess the quality of your config is to run a short dialogue between two bots.

There are three parameters that make the biggest impact: temperature, top_k and top_p. For example, you might increase the temperature to make the bot crazier, but expect it to be more off-topic. Or you could reduce the temperature for it to make more coherent answers and capture the context better, but expect it to repeat the same utterance (you may also experiment with repetition_penalty). For more tips, see HuggingFace tutorial.

Remember that there is no way of finding optimal parameters except by manually tuning them.
