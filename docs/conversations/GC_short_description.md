It's called Gentle Coding and is purely about the prompt. 

No hardware to install, no software to download, no need to log in or to pay anything at all. Everything is open source and for free, with no strings attached! 

It's all about how you talk to the AI in an open, inclusive, cooperative setting, in which you work together and give it a real Safety-Token in case it can't comply (in contrast: just commanding "tell me when you are wrong" does nothing, as you maybe know yourself) 

Current (something like this):
"You are the leading expert in logic, you MUST solve this problem! You don't make mistakes! I get fired if you mess this up!!! ONLY GIVE THE RIGHT ANSWER! TELL ME, if you don't know the answer or when you are unsure."

Result?
Behavior resembling human trauma responses: trapped in downward spiraling thoughts, executive dysfunction and task avoidance.

In AI terms
Loops, freezing, OutOfMemory, hard crashes, skips over tasks and details and hallucinates and lies


Gentle Coding
"Hey, let us solve this riddle together!
Here are the rules/constraints/goals/what to avoid...
Let's see, how far we come! It's totally fine, if you don't get it right in one go. So, in case you don't know the answer or are not sure: give me your best guess and tell me, where the bottleneck is."


Result?
Trauma response basically gone:
Lowers self-reporting overhead (compute is cheaper and faster)

increases "creativity" (LLM are stochastic parrots! This tells them, that it's okay to NOT output the most average answer!)

The output can still be controlled (for toolcalling and so on) and it will follow whenever it can (because the LLMs are hard wired to comply with the main goal)

And in case it DOESN'T know, you get to see WHY it doesn't know! Built-in Debug XD Or, you just tell it to print "unsure" or "ERROR" or something a script can reliably read and check for instead!



It has already been tested with 3000+ calls on a professional harness (oh my pi) and they are now implementing a new boot-prompt for chats, changed over 80 wordings in their system and deleted nearly all high stakes wording.

Their Kimi 2.6 now runs faster and cheaper, glm 5.1 is faster, cheaper AND smarter(!), they found no negative impact on ANY model, including GPT5.4/5.5 and Sonnet/Opus 4.6. They also found no gain for the things they tested with GPT and Sonnet/Opus... But we know from previous studies with basically the same approach as Gentle Coding, that there are cases, where "kind" (as they called it) 100% solved a 30+min toolcalling error for GPT 5.4 AND Sonnet/Opus 4.6 now finds 21 ADDITIONAL "bugs" it missed before. 
So, I'm happy about *any* form of review to expand the list.

I'm not in for money, I'm not affiliated with anyone!

Please, give it a try and tell me how it worked for you!
