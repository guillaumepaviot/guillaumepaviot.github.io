---
date: 2020-12-19T10:58:08-04:00
description: "Academic group project for a NGO"
featured_image: "/images/project-3/logo_plastibot.jpg"
title: "A chatbot talking about plastic"
---

This group project was an academic project for the NGO [The Sea Cleaners](https://www.theseacleaners.org). The goal was to develop a chatbot to make their FAQ more attractive.  
The requirements were :
- the chatbot could be integrated in a website
- the chatbot is interactive
- the code is readable and the bot is easy to use for non coder   

We choose to use Tensorflow to analyse the question and find and answer, and integrate it in Flask. The data (theme, different questions linked to this theme, different answers that the bot will use) is stored in a JSON file. To make the pocess of adding or changing questions, the client can use an EXCEL version of the file, that will be converted afte to a JSON file.  
The goal of the neural network is to find which theme the user is talking about accoding to the JSON file. Once trained, we export the model so that it can be used on the Flask page.
The demo webiste is very light, the backend only use a tokenizer and the traine dmodel to choose an answer from its data.  
After trainning, the accuracy of our bot is more than 90% on the 84 themes it was trained on, is quick to answer and intuitive to change for the client.  
In the end, the client chose our solution over the other group using a multiple questions choice bot.  

{{< figure src="/images/project-3/greetings.png" >}}
*An example of the bot greeting the user*

{{< figure src="/images/project-3/answers.png" >}}
*The bot answering the same question with different answers*