---
title: Week 5
week: 5
slug: week5
---

If Week 4 was about laying groundwork, Week 5 was about discovering just how much of that groundwork I could rip up and rebuild smarter. Early in the week, I explored a larger LLM, Granite 3.3 (2.5B parameters), and followed a LangChain tutorial on agentic RAG. It was decent, not production-level, but enough to make me realize something slightly embarrassing: I'd been accidentally recreating half of LangChain over the past few weeks. On the bright side, it meant I now understood the pieces deeply enough to trim away a ton of complexity.

That realization hit me one night during dinner and I ended up locking in super hard for like 5 hours and completetly rebuilding my pipeline around a much simpler approach: using a vector database and a k-NN-based encoder to handle tool selection and slot filling. The result is something surprisingly powerful, something like a lightweight Siri-for-missions. It's faster, leaner, and often outperforms the full LLM-based approach in practical scenarios. Huge win.

On the project coordination side, I had yet another direction-setting meeting, but this one felt actually really ended up with some useful infromation. I shifted focus to integrating my chatbot into ADAPT GO and got it running with real functionality, including generating and editing human constraint objects on the fly.

I also cleaned up the UI and polished the interaction between ADAPT and my NLP model. I now have a personal GitLab repo where I'm tracking the project and keeping things modular. One fun breakthrough was getting the bot to handle incomplete user instructions: like when someone says "add a task," and it follows up naturally to fill in the missing details. It's a small thing, but it really makes the system feel conversational.

There's still room for refinement. The slot filler struggles with subtle semantics — like confusing "set Raptor 2's priority to 5" and interpreting it as priority 2. I'm experimenting with regex and semantic cues for now, but I may later explore training a more robust model with LLM-generated synthetic data. I'm also starting to think about Chain-of-Thought-style reasoning and how to incorporate pre-planning logic without making the system too slow or brittle.

Overall, this was my most transformative week yet. I tore down and rebuilt the pipeline, implemented key ADAPT integrations, and came away with a system that's already looking solid for demos. There's a long road ahead, but I'm starting to see how this all fits together — and I'm genuinely excited to keep pushing.
