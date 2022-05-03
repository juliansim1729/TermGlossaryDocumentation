---
title: Project Updates
date: 2022-04-02
tags:
  - Weekly Check In
  - Week12
  - Updates
layout: layouts/post.njk
---
# Week 12 Progress

## End Points (Back-End + API/PM)

We are currently working off of a two endpoint plan and seek to keep/expand it in the future based on our changing needs.

vocab.js
- Located in /api
- Communicates with Planetscale and our microfrontend
- It requires an action from our microfrontend (CREATE or READ)
- Returns all vocab words, one vocab word, or creates a new vocab word in Planetscale based on action input

vocab-term.js
- Located in /src
- Gets values/button clicks from frontend, processes them to go to Planetscale or to be shown on frontend, and communicates with vocab.js to work with Planetscale
- It requires input from the frontend (word, description, any links to create word, an HTML element to 'define' with vocab, option to show all vocab)
- It returns a single vocab-term formatted element to the frontend or every vocab-term at once

Currently, we are focusing on vocab-term.js. We have currently created a sample response within our render function for primary testing, although we have also created the frameworks that should allow for it to easily become generalized. Some of this work can be seen [here](https://github.com/zjohnson10/final-project-vocab/blob/main/src/vocab-term.js).

## Front-End Assets 

Going off of the structure we created through Adobe Dreamweaver, and a new tool called Nicepage Desktop, we were able to start adding in our assets into the overall front-end structure. The simple "waterfall" design of the web page allows for easily compartmentalizable sections that can be quickly adjusted without affecting the entire document. 

We can see this design implemented [here](https://front-end-attempt2.vercel.app/#) (although it may be updated in future releases, making the explanation that follows obsolete!)

Our header serves as the first section, with an appealing animation to give our microservice a fun and appealing vibe. 

Then, we create the glossary input service in the red section. This section enables the user to submit words, definitions, and links into the overall glossary. The Add Word button, once clicked, then transmits that information into the back-end database to store. We made the button a similar color to the red that delineates the section, adding in a slight gradient in order to make the button spiffy and rad. The final asset we chose to use was an animated picture of a beach to give the section a pleasing and relaxing cool vibe (in both terms of color and attitude) to make the user feel happy and comfortable when using our application. 

The final section, in a contrasting and pleasing blue, focuses on the other service of the word glossary. It seeks to intake in a sample of text and then reference the glossary for words contained in the text that are defined. The button then sends the information to the back-end, where the text is first searched for words in the glossary, and then returns back an annotated version of the text for the user to see. 

We also include a way to see the full glossary in the page. When the button is clicked, it will redirect the user to a page containing the full glossary. The happy animations within this section help the user to feel confident and comfortable in accessing the full glossary showing them that learning about vocab is fun and entertaining after all.

Currently, code for both the "Add Word" and "Process" buttons are in the process of being implemented, while the "View Glossary" button is a later priority. We understand that the visuals may distract from the development, so a "low-tech" version of our app also exists, which has no unnecessary bling and can be used for focused development and testing. Some of this code is contained [here](https://github.com/ParkerEM/final-project-vocab/tree/frontend).
