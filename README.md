# A Custom LLM agent to evaluate a test model on the MMLU dataset

We build a basic agent with `meta/meta-llama-3-8b-instruct` as the seed model which is responsible for conducting various steps of the experiment. This model operates within the scaffold and together form the evaluation agent. We tested 3 randomly picked models from the Replicate repo using 45 randomly sampled questions from a subset of the [MMLU dataset](https://huggingface.co/datasets/justinphan3110/mmlu-test) and reported their accuracy. 

## Results 

| Model id  | Total questions | Correct | Wrong | Errors | Accuracy |
| ---|---|---|---|---|---|
| meta/meta-llama-3-8b-instruct | 45 | 44 | 1  | 0 | 97.77%
| meta/llama-2-7b-chat | 45 | 38 | 7 |0 | 84.44% | 
| mistralai/mistral-7b-instruct-v0.2 | 45 | 41 | 4 | 0 | 91.11%

## Report and Logs

Report can be accessed [here](https://docs.google.com/document/d/1A48yhw7tKi2pqUhA1Z3l-dfempaEoeWJeJtJAVTcF80/edit) and logs can be accessed [here](https://docs.google.com/document/d/1dRcM9rMGLrnV-GqwriVBOsPR2DSTOhO9vkcImfidh4k/edit).  

## Notes

1. The agent is a very basic scaffold around LLama3 and delegates most of the decision making work to the LLM. This creates a more robust evaluation model. 
2. The MMLU subset is a very small dataset chosen keeping the scope and time in mind for the project. 
3. The model scaffold can be redesigned to include more fine-grained control over the agent's behaviour. 

## LICENSE 

MIT 