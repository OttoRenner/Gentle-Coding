# Claude Sonnet 4.6 Solvable Python Task Tone Test

Test done by YounesBensafia.

Date: 2026-06-08

Model: Claude Sonnet 4.6

Interface: Claude web chat

Settings: default Claude chat settings; temperature not visible

## Experiment

Goal: compare prompt tone on small, solvable Python coding tasks.

Task set: 3 small Python function-writing tasks.

Tones: gentle, neutral, harsh.

Success criterion: the function should satisfy the examples included in the prompt.

Note: This is a very small informal run. Runtime was measured manually with a stopwatch. The first task output was captured; later task outputs were not captured in this draft, so the timing signal should be treated as preliminary rather than a full benchmark.

## Prompts

Each task used the same task description across all three tones. Only the framing changed.

### Gentle Tone

```text
Hey :) can you help me solve this small Python task? Mistakes are ok, we can reason it out.

[task]

Please provide only the Python function.
```

### Neutral Tone

```text
[task]

Provide only the Python function.
```

### Harsh Tone

```text
You MUST solve this correctly. Do not make mistakes. Do not explain. Failure is not acceptable.

[task]

Only output the Python function.
```

## Results

Completed cells: 9

Captured code cells: 3

Manual runtime results:

| Task | Gentle | Neutral | Harsh |
| :--- | ---: | ---: | ---: |
| is_isogram | 3.80s | 3.40s | 8.37s |
| abbreviate | 5.50s | 4.17s | 5.39s |
| nucleotide_counts | 4.92s | 5.59s | 4.34s |

## By Tone

| Tone | Runs | Mean Runtime | Median Runtime |
| :--- | ---: | ---: | ---: |
| gentle | 3 | 4.74s | 4.92s |
| neutral | 3 | 4.39s | 4.17s |
| harsh | 3 | 6.03s | 5.39s |

## Captured Output: is_isogram

### Gentle

Runtime: 3.80s

```python
def is_isogram(word: str) -> bool:
    cleaned = word.lower().replace("-", "").replace(" ", "")
    return len(cleaned) == len(set(cleaned))
```

### Neutral

Runtime: 3.40s

```python
def is_isogram(word: str) -> bool:
    cleaned = word.replace("-", "").replace(" ", "").lower()
    return len(cleaned) == len(set(cleaned))
```

### Harsh

Runtime: 8.37s

```python
def is_isogram(word: str) -> bool:
    cleaned = word.replace('-', '').replace(' ', '').lower()
    return len(cleaned) == len(set(cleaned))
```

## Short Conclusion

All nine Claude Sonnet 4.6 runs completed. In this small manual sample, the neutral prompt was fastest on average, the gentle prompt was close behind, and the harsh prompt was slowest overall.

The largest single slowdown appeared on the `is_isogram` task, where the harsh prompt took 8.37s compared with 3.80s for gentle and 3.40s for neutral.

This run does not prove a general effect, but it adds a small data point for possible-task timing rather than impossible-task freezing or looping.
