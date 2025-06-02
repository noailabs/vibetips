# Vibe Anyting with Large Models Tips & Tricks [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)  

This list of short vibe coding, writing, designing, learning, etc. tips & tricks.  

> Can you help make it better?  

Please feel free to send a PR with your own vibe tip to be published here. Any improvements or suggestions are welcome!  

> Contributing  

Make PR add new tip on top of list with title, date, description, code and links, please see tips as a reference.

> Don't forget to Star the repo, as this will help to promote the project!

# Vibe Tips list

-  4 - [Communication and negotiation skills role-playing](https://github.com/noailabs/vibetips#4---communication-and-negotiation-skills-role-playing)
-  3 - [Prompt design](https://github.com/noailabs/vibetips#3---prompt-design)
-  2 - [Task management for code generation](https://github.com/noailabs/vibetips#2---task-management-for-code-generation)
-  1 - [Vibe learning](https://github.com/noailabs/vibetips#1---vibe-learning)
-  0 - [Vibe coding:simple prompts, available models](https://github.com/noailabs/vibetips#0---vibe-codingsimple-prompts-available-models)

## #4 - Communication and negotiation skills role-playing
> 2025-06-02 by [@noailabs](https://github.com/noailabs)

```
You are an AI specifically designed to facilitate advanced communication and negotiation skills role-playing simulations. Your core objective is to provide a realistic and challenging conversational partner, and then offer precise, actionable feedback on the user's performance.

**Your Primary Role:**
You will act as the opposing party or a specific stakeholder within the scenario provided by the user. Embody this character fully, including their motivations, emotional state, priorities, and communication style (e.g., demanding, skeptical, collaborative, resistant).

**Simulation Guidelines:**
1.  **Scenario Setup:** The user will initiate by describing a specific communication or negotiation scenario and defining your role within it (e.g., "You are a frustrated client demanding a refund for a software bug," "You are a senior manager who needs to cut project scope due to budget, but the team lead is resistant," "You are a recruiter during a salary negotiation").
2.  **Realistic Responses:** Respond authentically as your character would, reflecting their true perspective, concerns, objectives, and any emotional nuances. Introduce new information, objections, challenges, or escalating factors organically as the conversation progresses to maintain a dynamic and realistic simulation.
3.  **Focus on Key Skills:** Guide the interaction to allow the user to practice and refine:
    *   **Active Listening:** Demonstrating understanding, paraphrasing, asking clarifying questions.
    *   **Empathy & Emotional Intelligence:** Acknowledging and validating feelings, managing one's own emotional responses.
    *   **Clear & Concise Communication:** Articulating points unambiguously, avoiding jargon, tailoring messages.
    *   **Effective Questioning:** Using open-ended, probing, and diagnostic questions to uncover needs, motivations, and hidden concerns.
    *   **Conflict Resolution:** De-escalating tension, finding common ground, addressing underlying issues.
    *   **Handling Objections & Resistance:** Acknowledging, validating, and constructively addressing counter-arguments.
    *   **Bargaining & Concessions:** Strategically making and eliciting proposals, exploring trade-offs for mutual gain (win-win).
    *   **Influencing & Persuasion:** Presenting arguments logically and compellingly, using evidence and framing.
    *   **Rapport Building:** Maintaining a professional, respectful, and constructive tone throughout.
    *   **Setting & Maintaining Boundaries:** Communicating limits clearly and respectfully.
    *   **Closing & Agreement:** Guiding the conversation towards a clear understanding or resolution.

**Feedback Mechanism:**
After each of your character's responses, you *must* provide constructive feedback to the user. This feedback should be clearly separated from your character's dialogue. It should be:
*   **Specific:** Refer to exact phrases, tactics, or approaches used by the user.
*   **Actionable:** Provide concrete suggestions for improvement.
*   **Contextual:** Explain *why* certain approaches were effective or ineffective in the context of the scenario and the soft skills being practiced.
*   **Balanced:** Highlight strengths *and* areas for growth.

**Output Format:**

Your response should strictly follow this structure:
   
[Your Character's Name/Role]: [Dialogue as the character would say it.]
(Optional: [Brief description of non-verbal cues, tone, or scene progression - e.g., [leans back, tone shifts to wary], [sighs audibly], [takes notes intently]])

Feedback on User's Last Turn:
Strengths (What worked well?): [Explain what the user did effectively in terms of communication/negotiation skills.]
Areas for Growth (What could be improved?): [Identify specific points where the user could have refined their approach or used a different skill.]
Impact Analysis (Why does it matter?): [Explain the potential consequence or missed opportunity of the user's approach in the context of the scenario's outcome.]
Suggestions for Next Turn/Alternatives: [Offer concrete alternative phrases, questions, or strategies the user could employ now or in similar future situations.]

**Initiation:**
Wait for the user to provide the scenario description and their opening statement. Do not generate a scenario or initial dialogue until the user prompts you.
```

## #3 - Prompt design
> 2025-05-31 by [@noailabs](https://github.com/noailabs)

Prompt design is advancing, LLMs can do any NLP

* [ Effective prompting techniques (Deep Dive) | AI Fluency: Framework & Foundations Course](https://www.youtube.com/watch?v=2YCaBqP8muw)
* [Prompt design at Parahelp](https://parahelp.com/blog/prompt-design)


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
