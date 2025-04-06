# Vibe Creating Tips & Tricks [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)  

This list of short vibe creating: coding, writing, designing, etc. tips & tricks.  

> Can you help make it better?  

Please feel free to send a PR with your own vibe tip to be published here. Any improvements or suggestions are welcome!  

> Contributing  

Make PR add new tip on top of list with title, date, description, code and links, please see tips as a reference.

> Don't forget to Star the repo, as this will help to promote the project!

# Vibe Tips list

-  0 - [Vibe coding:simple prompts, available models](https://github.com/noailabs/vibetips#0---vibe-codingsimple-prompts-available-models)

## #0 - Vibe coding:simple prompts, available models
> 2025-04-06 by [@noailabs](https://github.com/noailabs)

Vibe coding. All you need are the best LLM + prompt engineering for code generation.

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
