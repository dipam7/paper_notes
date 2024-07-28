# Notes

Link to paper: https://arxiv.org/pdf/2405.14838

The paper talks about starting with CoT and then having the model internalize it. It uses the example of multiplying numbers which LLMs are traditionally bad at.
The first thoughts that come to mind when reading this paper are

1) Simple idea (which I love and am a fan of)
2) Mimics how humans learn? (as an intern I had to be told things but slowly they became intuition / second nature)

Even tho this method works well on certain tasks, further research is needed to explore its efficacy across a broader range of tasks and more diverse CoT traces.

In Stepwise Internalization you start with full CoT

For example

Stage 0: 21 * 43 = 8 4 + 0 6 3 = 8 0 4

Then at each subsequent stage, you remove 1 token from CoT and the model is finetuned to predict the rest of the tokens, eventually removing all CoT tokens and just getting the final answer

<img width="1149" alt="image" src="https://github.com/user-attachments/assets/94244619-825d-44c8-9af1-d7f7a1ca2a9f">

Before seeing the above example I thought this method is really smart but the way they remove a token at every stage seems suboptimal

Interesting that I read [this article](https://www.answer.ai/posts/2024-07-25-transformers-as-matchers.html) on the same day which also uses multiplication as a way of trying to show LLMs don't reason but just cache reason (pattern match)

TODOs:
- [ ] Check GSM8K dataset
- [ ] Checkout papers [6], [14] and [19] from references
- [ ] [6] "This method involves training a teacher model to perform explicit CoT reasoning and then transferring this knowledge to a student model, which internalizes the reasoning process within its hidden states" << how does this happen, learn more about it
- [ ] Did not understand this "The intermediate steps are also reversed to make it easier for the model to predict" (see paper 17 for more)
