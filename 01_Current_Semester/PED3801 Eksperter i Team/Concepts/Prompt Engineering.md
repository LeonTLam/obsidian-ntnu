---
tags:
  - Concept
---
# Concept for [[Landsbydag 7.md]]

# New Tasks Without Extensive Training

## Zero-Shot Prompting

Removes need for extensive training data. Instead, carefully craft prompt that guide the model. Generate predictions based on given prompt.

## Few-Shot Prompting

Provide few high-quality input-output examples to introduce an understanding of given task. Proven to improve model performance on complex tasks, but requires additional tokens, not befitting longer text inputs. Using examples may impose bias and influence model behaviour, such as favouring frequent words.

## Chain-of-Though (CoT) Prompting

Coherent and step-by-step reason processes. Demonstrates the effectiveness in more structured and thoughtful responses from LLMs.