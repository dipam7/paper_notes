# Notes

Follow up from paper_01, turns out 2 of the authors are the same

Explicit CoT / horizontal reasoning = when the model produces CoT tokens and then produces a final answer
Implicit CoT / vertical reasoning = use the hidden layers of a model to reason and then directly produce the final answer

Teacher model which produces explicit CoT tokens and it's hidden states are used to train an emulator.
A student model that is trained to use another model (teachers' or emulators') hidden states to produce the final output

While I understood the overall concepts, the actual implementation was tricky to understand, might have to look at code

It seems hacky rather than simple

TODOs:
- [ ] Come back to this paper / look at the code
