---
date: 2020-12-19T10:58:08-04:00
description: "Academic group project for a NGO"
featured_image: "/images/project-3/logo_plastibot.jpg"
title: "A chatbot talking about plastic"
---

This academic group project, conducted for the NGO [The Sea Cleaners](https://www.theseacleaners.org), was aimed to develop a chatbot to enhance the attractiveness of their FAQ section.

**Key Requirements:**

-Integratable into a website
-Interactive and user-friendly
-Readable code and easy-to-use for non-coders

**Implementation Details:**

**-Technology Stack**: We used TensorFlow for question analysis and Flask for integration.
**-Data Management**: Themes, questions, and answers are stored in a JSON file. For ease of modification, clients can use an Excel version of the file, which is later converted to JSON.
**-Neural Network Goal**: The neural network identifies the theme of the user's question based on the JSON file. Once trained, the model is exported for use on the Flask page.
**-Backend**: The lightweight demo website uses a tokenizer and the trained model to select answers from its data.
**-Frontend**: The website is built with simple HTML, CSS and Javascript.

**Performance and Outcome:**

-The chatbot achieved over 90% accuracy across 84 trained themes.
-It is quick to respond and easy for the client to update.
-Our solution was chosen by the client over a multiple-choice bot developed by another group.

This project was a big success, both in terms of the solution we developed and in terms of how it went as a group.

{{< figure src="/images/project-3/greetings.png" >}}
*An example of the bot greeting the user*

{{< figure src="/images/project-3/answers.png" >}}
*The bot answering the same question with different answers*