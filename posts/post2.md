---
title: API
description: Generally how the API works. 
date: 2022-05-01
tags: 
layout: layouts/post.njk
---

## API Design
Naturally, when creating this project, we had to lean heavily on the usage of APIs. For that matter, we utilized OpenAPI 3.0 from Swagger, which can be found [here](https://github.com/zjohnson10/final-project-vocab/blob/main/openapi.json). This document was utilized to create the following API endpoints, alongside how they are leveraged by the code.

## API Endpoints

### addWord.js
- Located in /api
- Communicates with Planetscale and our microfrontend
- It requires an action from our microfrontend (CREATE)
- Creates a new vocab word with a definition and any links in Planetscale

### getWord.js
- Located in /api
- Communicates with Planetscale and our microfrontend
- It requires an action from our microfrontend (READ)
- Returns one word with it's description and any links from Planetscale

### getWords.js
- Located in /api
- Communicates with Planetscale and our microfrontend
- It requires an action from our microfrontend (READ)
- Returns all words with their descriptions and any links from Planetscale

### processWords.js
- Located in /api
- Communicates with planetscale and our microfrontend
- It requires an action from our microfrontend (READ)
- Returns the words that have vocab definitions from Planetscale

### removeWord.js
- Located in /api
- Communicates with Planetscale and our microfrontend
- It requires an action from our microfrontend (DELETE)
- Deletes specified word from Planetscale

### vocab-term.js
- Located in /src
- Gets values/button clicks from frontend, processes them to go to Planetscale or to be shown on frontend, and communicates with vocab.js to work with Planetscale
- It requires input from the frontend (word, description, any links to create word, an HTML element to 'define' with vocab, option to show all vocab)
- It returns a single vocab-term formatted element to the frontend or every vocab-term at once