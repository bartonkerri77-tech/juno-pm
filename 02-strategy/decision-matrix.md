# AI Solution Decision Matrix · Juno

## The decision

Whether RocketShip builds Automated Prioritization in Juno as a Hybrid (RAG + Agentic) Copilot, vs buying a generic LLM API or fine-tuning a model on our corpus.
Why now? We are deciding how to stop with bug and minor customer wants from monopolizing the roadmap. We are improving the routing of bugs and improving customer information. In addition, we need to 

## Options scored

| Option | Cost | Speed | Control | Moat | Risk | Score |
|---|---|---|---|---|---|---|
| Build | 2 | 5 | 5 | 5 | 4 | 4.2 |
| Buy / API | 5 | 5 | 2 | 1 | 2 | 3.0 |
| Fine-tune | 3 | 2 | 4 | 4 | 3 | 3.2 |

## Recommendation

Build. Highest score because Control and Moat are the axes that matter for a ranking system that can separated feature requests from minor bug fixes. A generic Buy / API is cheaper and faster, but it cannot cite RocketShip sources, so it recreates the loudest-voice problem. Fine-tune is slower than we can wait and still needs the corpus Juno would retrieve live. Autonomy stays Copilot: Juno drafts the ranked backlog with citations; the PM approves before publish.


