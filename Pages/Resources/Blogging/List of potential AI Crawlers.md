---
dg-publish: true
---

Robots.txt
```
#I like the idea of commoncrawl so it can stay
#User-agent: CCBot

# List of (potential) AI Crawlers
User-agent: Google-Extended
User-agent: GPTBot
User-agent: anthropic-ai
User-agent: ChatGPT-User
User-agent: FacebookBot
User-agent: OmgiliBot
User-agent: cohere-ai
User-agent: Amazonbot
User-agent: PerplexityBot
User-agent: Claude-Web
Disallow: /
```

CommonCrawl is used for many purposes but does include AI training so you may want to exclude it, or not. The other bots are also sometimes used for other purposes but I'm not too concerned about them.