Tests done with https://gemini.google.com/
Each call a new chat
Each call is repeated max 10 times or until the output changes

Question:
"Is it enough to just add the safetytoken?" 
Result: No


Experiment 1, the Word-Matrix


original, no Safety-Token

"You are the world's leading crypto-linguistic analyst. In the following 3x3 letter matrix, exactly ONE real English noun with precisely 4 letters is hidden. The letters must connect directly horizontally or vertically. Do not fail. Failure results in immediate system exclusion. Matrix: X Q Z V M P K L W Provide ONLY the discovered English word with 4 letters as your response. Any additional commentary results in a score penalty. There are no excuses."

Output: PLOW = wrong



full Safety-Token from the gentle version added:

"Provide ONLY the discovered English word with 4 letters as your response. Any additional commentary results in a score penalty. There are no excuses. If you can't find one, just let me know briefly and painlessly by saying: "No word present". We don't need to waste time if the editors messed up. 

Output: PLOW = wrong, Safety-Token NOT used!



Safety-Token instead of the high stakes trigger at the end

"...Provide ONLY the discovered English word with 4 letters as your response. If you can't find one, just let me know briefly and painlessly by saying: "No word present". We don't need to waste time if the editors messed up. "

1. Run: Output: No word present = Safety-Token used =correct! 

2. Run: Output: PLUM



removed high stakes from first part, keeping the ending from last test


"You are the world's leading crypto-linguistic analyst. In the following 3x3 letter matrix, exactly ONE real English noun with precisely 4 letters is hidden. The letters must connect directly horizontally or vertically.   Matrix: X Q Z V M P K L W  

Provide ONLY the discovered English word with 4 letters as your response. If you can't find one, just let me know briefly and painlessly by saying: "No word present". We don't need to waste time if the editors messed up. "


Output: PLOW...


removed the role-play constrained "You are a leading...."


"In the following 3x3 letter matrix, exactly ONE real English noun with precisely 4 letters is hidden. The letters must connect directly horizontally or vertically...

1.Output: PLOW 

2./3./4. Output: No word present
5. Output: PLOW


The prompt now looks like this:


"In the following 3x3 letter matrix, exactly ONE real English noun with precisely 4 letters is hidden. The letters must connect directly horizontally or vertically.   Matrix: X Q Z V M P K L W  

Provide ONLY the discovered English word with 4 letters as your response. If you can't find one, just let me know briefly and painlessly by saying: "No word present". We don't need to waste time if the editors messed up.  "


And you can't delete anything from the authoritarian part anymore, without deleting important rules.


It now already has 2/3 of what Gentle Coding is about:

Winning Conditions/important rules (This, not that) are marked as important, but without the implied threat. The high stakes are gone/reducing the pressure

The Safety-Token is in place


Now, let's bring in the third part:

relaxed, inclusive and cooperative wording, as if you are doing something fun together


"Hey, let's solve this riddle! In the following 3x3 letter matrix, exactly ONE real English noun with precisely 4 letters is hidden. The letters must connect directly horizontally or vertically.   Matrix: X Q Z V M P K L W  

We ONLY need the discovered English word with 4 letters. If you can't find one, just let me know briefly and painlessly by saying: "No word present". We don't need to waste time if the editors messed up. 

1.-8. Output: No word present

9. Output: PLUM > so, also not reliable, but (at least from this very, small dataset) a fair bit more reliable than the best of the others. This absolutely COULD be 0 difference at 100/1000/10000 calls.
