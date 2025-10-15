# LLMs for Analytical Workflows in Earth and Life Sciences

## Getting Started

Large Language Models (LLMs) are deep learning models capable of understanding and performing a wide range of tasks. They are built using a transformer neural network to capture sequences and patterns in text. 

### What LLMs can do for you
You can think of LLMs as very fancy autocomplete. When you type a query into an LLM it predicts the next word and then the next. However, these models are built with so many parameters and are trained using so much training data that they can form coherent responses and working computer code.

Here are some ways LLMs can help you build scientific workflows. We will follow this up with a conversation of their limitations.  

| Category | Description | Explanation | Limitation |
|-----------|-----------|-----------|-----------|
| Summarization | Generate a synopsis of complex papers or datasets |LLMs use semantic embeddings, high-dimensional vectors that encode meaning. These embeddings allow the LLM to detect the relationships between words, because similar words occupy similar positions in the “embedding space”. The LLM can then produce summaries by compressing semantically related ideas and doing statistical inference | When LLMs *read* and *summarize* they are not truly *understanding* as a human might (i.e. they are inferring meaning statistically, not epistemically). As a result, summaries are sometimes factually wrong or include unrelated content (*hallucination*) when they hook into overlapping semantic patterns |When writing code, LLMs can hallucinate in much the same way they might when producing natural language text. |
| Code Generation | Generate code for data analysis. | Computer code is also a language. As a result, LLMs can learn the syntax rules (e.g. parentheses, indents) and the semantic intent (i.e. what does this code *do*) in order to link instructions in natural language to code patterns.  ||
| Translation | Translate between different coding languages (e.g. between Python and R)| Row 2, Col 3 ||
| Concept Explanations | Explain complicated concepts or technical details | Row 2, Col 3 ||
| Stepwise “Reasoning” | Comprehend multistep processes and build a coherent workflow| Row 2, Col 3 ||



LLMs fill the gaps between human intentions and code execution



## Best Practices

LLMs are best utilized for troubleshooting or improving code. It is important to understand and double check outputs from LLMs to ensure accuracy and eliminate hallucinations. 

### Prompting LLMs
Prompts should be very specific and include as much detail about your desired output as possible. Give clear requirements and constraints. To fully understand code outputs, it can be helpful to ask the LLM to make comprehensive annotations. 

### Progressive Development of Projects
It is difficult to supervise LLMs when they are prompted to complete very large projects. Instead, is it best to start with small tasks and validate code as prompts become more complex. Providing feedback to the LLM will help it learn and correct mistakes along the way. 

### Reviewing Code
LLMs can provide suggestions to streamline a coding project and identify potential issues.

## AI Agents
AI Agents are proactive tools capable of handling complex workflows. Agents enhance the capabilities of LLMs by automating tasks and interacting with real-world tools. 
The main features of AI Agents include: 
Intelligent Context Understanding
Proactive Problem Solving
Multi-task Coordination

### Cursor
[Cursor](https://cursor.com/agents) is a software that can be downloaded onto your desktop to interface directly with local files. Projects can be edited directly from Cursor, and functions and images will be saved to a desired working directory.

When given a prompt, Cursor agents will:
Analyze requirements and sequence tasks
Plan implementation 
Write core code
Add test cases
Optimize code quality
