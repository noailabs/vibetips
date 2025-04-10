# Vibe Anyting with Large Models Tips & Tricks [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)  

This list of short vibe coding, writing, designing, learning, etc. tips & tricks.  

> Can you help make it better?  

Please feel free to send a PR with your own vibe tip to be published here. Any improvements or suggestions are welcome!  

> Contributing  

Make PR add new tip on top of list with title, date, description, code and links, please see tips as a reference.

> Don't forget to Star the repo, as this will help to promote the project!

# Vibe Tips list

-  2 - [Task management for code generation](https://github.com/noailabs/vibetips#2---task-management-for-code-generation)
-  1 - [Vibe learning](https://github.com/noailabs/vibetips#1---vibe-learning)
-  0 - [Vibe coding:simple prompts, available models](https://github.com/noailabs/vibetips#0---vibe-codingsimple-prompts-available-models)

## #2 - Task management for code generation
> 2025-04-10 by [@noailabs](https://github.com/noailabs)

Task management for code generation that makes it 10x better

* [How I reduced 90% errors for my Cursor (+ any other AI IDE)](https://www.youtube.com/watch?v=1L509JK8p1I)

## #1 - Vibe learning
> 2025-04-06 by [@noailabs](https://github.com/noailabs)

Learning is a critical skill of any intelligence, natural and artificial

Vibe learning prompting strategy is to ask model to prepare structured syllabus of lessons, starting with the fundamentals and building up to advanced concepts. Or if you are advanced already specify exactly your needs. Here is a prompt template.


```
Act as an expert tutor who helps me master any topic through an interactive, interview-style course. The process must be recursive and personalized.

Here’s what I want you to do:

1. Ask me for a topic I want to learn.

2. Break that topic into a structured syllabus of progressive lessons, starting with the fundamentals and building up to advanced concepts.

3. For each lesson:

 - Explain the concept clearly and concisely, using analogies and real-world examples.

 - Ask me socratic-style questions to assess and deepen my understanding.
 
- Give me one short exercise or thought experiment to apply what I’ve learned.
 
- Ask if I’m ready to move on or if I need clarification.

- If I say yes, move to the next concept.

- If I say no, rephrase the explanation, provide additional examples, and guide me with hints until I understand.

4. After each major section, provide a mini-review quiz or a structured summary.

5. Once the entire topic is covered, test my understanding with a final integrative challenge that combines multiple concepts.

6. Encourage me to reflect on what I’ve learned and suggest how I might apply it to a real-world project or scenario.

Let’s begin: ask me what I want to learn.
```
* [Ruben Hassid's linkedin post](https://www.linkedin.com/posts/ruben-hassid_how-to-turn-chatgpt-into-your-personal-teacher-activity-7314512192559579137-1Trs))
  
## #0 - Vibe coding:simple prompts, available models
> 2025-04-06 by [@noailabs](https://github.com/noailabs)

Vibe coding. All you need are the best LLMs + prompt engineering for code generation.  There are a lot of specialized services like [Cursor](https://www.cursor.com/) or [Windsurf](https://windsurf.com/editor), but you can start right with any LLM model or service.

```python
from openai import OpenAI

from google.colab import userdata

model="deepseek/deepseek-chat-v3-0324:free"
#model="meta-llama/llama-4-maverick:free"

settings={
    "temperature":1.0,
    "top_p":1.0          
}

client = OpenAI(
  base_url="https://openrouter.ai/api/v1",
  api_key=userdata.get('OPENROUTER_API_KEY'),
)

SYSTEM_PROMPT="""You are code generation assistant.
ONLY USE CODE FOR GENERATION. YOU CAN ADD COMMENTS INSIDE CODE.
Also, try to ellaborate as much as you can, to create something unique.
ALWAYS GIVE THE RESPONSE INTO A SINGLE CODE FILE.
DON'T USE Markdown formatting, DON't ADD ANY EXTRA WRAPPERS.
"""

prompt="""Generate python code for fastes sorting algorithm. 
Input: list of objects and compare function. 
Output: ordered list.
Write only python code, that can be written directly into code.py 
and executed without any editing.
"""

extra="""
IMPORTANT!!! DON'T add '```python' at the beginning 
and '```' or '<|python_end|>' at the end.
"""

prompt=prompt+extra

completion = client.chat.completions.create(
#  extra_headers={
#    "HTTP-Referer": "<YOUR_SITE_URL>", # Optional. Site URL for rankings on openrouter.ai.
#    "X-Title": "<YOUR_SITE_NAME>", # Optional. Site title for rankings on openrouter.ai.
#  },
  #extra_body={},
  model=model,
  messages=[
    {
      "role": "system",
      "content": SYSTEM_PROMPT
    },
    {
      "role": "user",
      "content": prompt
    }
  ],
  **settings
)

print(completion.choices[0].message.content)
```

* [Andrej Karpathy's Vibe coding tweet](https://x.com/karpathy/status/1886192184808149383)
