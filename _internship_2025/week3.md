---
title: Week 3
week: 3
slug: week3
---

I figured I'd start this week's post by diving deeper into my project. The core idea is to build a modular LLM pipeline that can integrate easily with other systems. Up until this week, my pipeline could:

- Take in JSON data, convert it to SQL, and append it to a database
- Accept a server-side question about the data, generate an SQL query with an LLM, query the database, and return the results — all server-side

This basic version worked but had several flaws and missing pieces. So this week, I focused on expanding its capabilities. I added:

- Live data streaming into the database
- Support for imperative (action-based) input
- An LLM module to turn raw data into natural language
- A simple speech-to-speech pipeline
- Client-side question-and-answer capability
- A full architecture redesign to make the whole pipeline more modular and developer-friendly

Getting live data flow working meant digging into HTTP requests, port forwarding, and optimizing speed and bandwidth. I designed a batching system to send data in chunks instead of one item at a time, which made a big difference.

The imperative input feature started out simple: I used a small LLM, did some prompt engineering to pick actions from a list, and parsed the output. But by the end of the week, I overhauled it completely. Originally, adding a new action required editing multiple files and wasn't intuitive. Now, with a cleaner object-oriented approach, I created an `Action` class. Developers can simply extend this class to define new actions — with a name, description, example, and the actual code to run. An `ActionDispatcher` handles registering and calling them. This is much more elegant and I'm very happy with the outcome.

The speech-to-speech pipeline was surprisingly straightforward. I used OpenAI's Whisper Small for speech-to-text and a separate text-to-speech model, then connected them — a good example of how clear pipeline design makes life easier. The size of these speech to text models blew me out of the water. I mean speech to text is halfway magical and these models are in the low millions of parameters!

The biggest challenge of the week, by far, was setting up the client-side question and answer system. Without getting too deep into the weeds: I needed two servers to communicate securely, which required port forwarding and a custom proxy server to handle traffic. It took a full day of troubleshooting, overhauling, rubber ducking with Daniel, and two hot chocolates, but it finally worked.

Overall, this week really pushed me to apply and expand my knowledge across multiple areas — and I'm excited to keep improving this system.
