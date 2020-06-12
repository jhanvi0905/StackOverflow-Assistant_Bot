# StackOverflow-Assistant_Bot

Description-

The bot is a helper bot for navigating the site of StackOverflow. The bot searches the best threads matching the user query and guides the user towards the link of that thread.

Training-

1. NLU part of Chatbot- The NLU model consist of two parts, intent recognizer and tag classifier both of which are trained as models and saved as .pkl files. The intent classifier is trained using the logistic regression, the tag classifier is trained using logistic regression as well however using the wrapper of One Vs Rest Classifier as there are 10 classes of tags.

2. Dialogue Generation Model- 
Considering the memory constraints, the dialogue generation model is trained based on pre-trained model from the chatterbot module.

3. Best Thread Ranking-
The threads are ranked on the basis of starspace embeddings trained previously on the StackOverflow data.

Deploying of the Bot-

The bot is deployed on telegram. The backend is running on the Ubuntu EC2 instance on the AWS server (free tier services). An instance of conversation is present in the repository as the image.
