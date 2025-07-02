# Train your chatbot service
In this project, we will fine-tune a GPT-2 model to become an English-language chatbot service and deploy it on Telegram for testing.

This project has used:

    + Gpt-2 pretrained model 124M params.

    + [Attention Is All You Need](https://arxiv.org/abs/1706.03762)

    + Parameters set to optimize model retraining speed (Recommended not to change).

    + Custom dataset. You can create your own training data tailored to your specific case in the form of question-answer pairs and save them into customer_service_questions and customer_service_answers.

    + This project also includes LoRAFineTuning using LoRALinear. However for better results I didn't use it in this case.

⚠️ Note: Multi-GPU traiing is not support for now. But to optimize training speed you should install.


## Install

1. First you need to change the training data in your case. Edit the DataLoaderLite class if needed to load the data.

2. Then run notebook step by step. You may modify the parameters; however, I do not recommend it unless you have a good understanding of them.

3. After retraining the model, to connect it to your Telegram bot, you need to replace the bot’s API token and save it in BOT_TOKEN

💥 Bang, your bot is ready! Now you just need to install some additional anti-DDoS measures and do a bit of magic to deploy your bot on the server, then it’s ready to serve 🚀

⚠️ Note: The training results will be highly dependent on the quality of the training data. So make sure your data is large enough and well filtered.