---
title: Micro Front End Operations
description: Generally how the micro front-end works
date: 2022-05-02
tags: 
layout: layouts/post.njk
---

## Project Goal

The goal of this project was to create a 'term glossary'. The term glossary microservice  seeks to present vocabulary based on what a user adds to a page. This draws on previous work which created methods to present vocabulary terms in context of the given material, linked here. Therefore, the project seeks to be able to dynamically store and process vocabulary terms to improve a user's productivity. Therefore, a user needs to be able to add (and remove) words, as well as view all the words.

## Add Word Userflow
![Add Word Userflow](https://i.ibb.co/GdVNzmy/addword.png)

First, we examine the Add Word userflow. A 'word' in our term glossary consists of the word itself, a description or definition of the word, and any relevant links. For example, if our word was *coffee*, then we could put in *hot bean juice with a shot of caffeine* as our description, and *starbucks.com* in for our link. Then, once the user presses the "Add Word" Button, this information would get sent to the back-end. There, the system would be able to read in the information, and then convert it to JSON format to allow for easier storage. Then, it would use SQL commmands to create a new word within the PlanetScale database. 

## View Word Userflow
![All Vocab Userflow](https://i.ibb.co/ng73Rxg/allvocab-drawio.png)

Next, once a few words have been submitted into the database, a user might forget some of them, and wonder what words were submitted. To that purpose, a user can click on the "Show All Words" Button within the site, which would then trigger the back-end to send a SQL command to retrieve all the words from the PlanetScale database. Having done so, it would convert the JSON data to HTML data for each word, which would also contain its definition and links. This information would be sent back to the front-end where the elements would then be able to be displayed.

## Delete Word Userflow
![Delete Word Userflow](https://i.ibb.co/YbVcYBL/Screenshot-72.png)

From here, once we have viewed a list of all the words, we can now delete any that we wish to remove. The user can click on the "Delete Word" button next to a word, which would then trigger the back-end to delete that specific word from the PlanetScale database utilizing SQL commands. Then, it would remove the HTML relating to that word, and re-return it to the Front-End, which would then re-render the word list.

## In Combination
These three main processes work in conjunction to allow a user to interact with a vocab glossary. They can add, view, and remove terms at their leisure, satisfying the project goals neatly.