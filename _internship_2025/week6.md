---
title: Week 6
week: 6
slug: week6
---

This week started off rough. I hit a wall of uncertainty... not technical, but directional. The tasks I had lined up (confidence thresholds, parallel instructions) felt more like maintenance than innovation, and I wasn't excited to work on them. I kept circling the same question: what exactly should it do? The answer didn't come quickly, and it left me feeling pretty stuck.

I filled some of that time doing light work: tweaking slides, reading papers, adding a feature here and there (like handling low-confidence queries gracefully). But it wasn't until later in the week that things finally started clicking again. I cleaned up the tool system, refactored big parts of the pipeline, and got the project running locally with database integration (a surprisingly satisfying milestone). Presenting to Andrew helped too, even if his reaction was more politely intrigued than wowed.

One key turning point was running into major issues when using actual entity IDs. The model began hallucinating parameters and tools, and nothing behaved the way I expected. That frustration drove me to rebuild AGAIN. And through some more research, I learned about zero-shot intent classifiers and realized that was *exactly* what I needed. I got one running and, for once, it just worked. It wasn't perfect, but it worked out of the box. So, I built fallback mechanisms and eventually landed on a really cool, new architecture.

Instead of relying on a single model with confidence thresholds, the new pipeline pools together multiple intent-scoring strategies: zero-shot classification, keyword matching, semantic similarity, spaCy pattern matching, and more. I score each method individually, weight them, and then rank to find the best match. It's ensemble intent classification and it's shockingly effective. The system is now both more accurate and more resilient. It's also way more satisfying to use.

Despite the slow start and occasional "why am I doing this" moments, this ended up being one of the most productive weeks yet. I still have bugs to squash and weird behaviors to figure out, but the pipeline feels smarter, cleaner, and closer to something I'd be proud to demo. That's a good place to be heading into the final stretch.
