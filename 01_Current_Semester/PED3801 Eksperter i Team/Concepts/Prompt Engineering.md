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

Coherent and step-by-step reason processes. Demonstrates the effectiveness in more structured and thoughtful responses from LLMs. CoT prompting allows users to guide LLMs through a logical reasoning chain, allowing you to reflect and gain a deeper understanding of the given prompt.

## Chain-of-Knowledge (CoK) Prompting

Traditional prompting techniques proven powerful for basic tasks, but diminishes due to reliance on fixed knowledge sources. CoK systematically breaks down tasks into cordinated steps. 

* Comprehensive reasoning preparation stage
	* Where context is established and problem is framed
* Dynamic knowledge adaption phase
	* Meticulously gathering evidence from various sources
