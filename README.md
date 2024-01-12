# Meta Prompting
Meta Prompting for AGI Systems

**Meta Prompting (General Definition)**: Meta Prompting is a prompting technique inspired by type theory, emphasizing the structure and syntax of examples rather than their detailed content. It's an approach where the focus is on presenting the outline or framework of a problem or topic, offering a scaffold that can be filled with specific details as needed. This technique is particularly useful in situations where understanding the form and pattern of a problem or solution is more crucial than the specific content.



## CR Agent Assistant v0.1 based on `Meta Prompting`

See `./cr-agent-assistant-v0.1.md` for a minimalist implementation based on OpenAI Assistant API.

- please visit [https://chat.openai.com/g/g-L3a4ZCIHx-cr-agent-v0-1](https://chat.openai.com/g/g-L3a4ZCIHx-cr-agent-v0-1) for an online demo.

See `./cr-agent-xml-assistant-v0.1.xml` for a minimalist XML-style implementation based on OpenAI Assistant API.

- please visit [https://chat.openai.com/g/g-4ir4la2Z6-cr-agent-xml-v0-1](https://chat.openai.com/g/g-4ir4la2Z6-cr-agent-xml-v0-1) for an online demo.

See `./cr-agent-xml-assistant-v0.2.xml` for a minimalist XML-style implementation based on OpenAI Assistant API.

- please visit [https://chat.openai.com/g/g-cJV031wLP-cr-agent-xml-v0-2](https://chat.openai.com/g/g-cJV031wLP-cr-agent-xml-v0-2) for an online demo.

The prompt of CR Agent XML v0.2 is autonomously generated by CR Agent v0.1 (this process can be seen as metaprogramming).

### Characteristics of Meta Prompting:

1. **Syntax-Oriented**: The emphasis is on the form and structure of the prompt. The syntax acts as a template or a guide that outlines how a response or solution should be structured.

2. **Abstract-Example-Based**: Abstracted examples are employed to demonstrate the structure, though they are not elaborated in the content. These examples act as frameworks for inserting specific details.

3. **Type Theory Inspiration**: Drawing from type theory, this approach focuses on the types or categories of components in a prompt, such as problem statements, solution steps, or conclusions, and how they are logically organized.

4. **Adaptability**: The approach is adaptable to various domains, from mathematical problem-solving to creative writing, where the structure of the response is a key element.

5. **Guidance for Detailed Exploration**: While it does not delve into specifics, Meta Prompting provides a clear pathway for detailed exploration, guiding users on how to approach and structure their deep dive into the topic.

### Application:

- **Use Case**: This is particularly beneficial in educational settings, programming, complex problem-solving, and areas where the process of thinking or the method of approach is as important as the answer itself.

- **Educational Tool**: In teaching, Meta Prompting can help students understand how to structure their thoughts and responses, providing a clear model for organizing information.

- **Problem-Solving Framework**: In complex problem-solving, it offers a blueprint for breaking down and tackling each part of the problem methodically.

In essence, the general concept of Meta Prompting is about providing a skeleton or a blueprint that outlines the structure of a response or solution, focusing more on the "how" rather than the "what" of information presentation. This method is especially useful in contexts where understanding the underlying structure is key to mastering the content or solving the problem.

---

**"Meta Prompting for Complex Reasoning"** is a specialized adaptation of the general Meta Prompting approach, specifically tailored for tackling intricate and multifaceted problems, particularly in fields requiring in-depth analytical and logical reasoning. This version emphasizes not just the structure and syntax of the problem-solving process, but also delves deeply into the content, ensuring a thorough and comprehensive approach to each problem.

### Key Elements of Meta Prompting for Complex Reasoning:

1. **Complex Problem Decomposition**: The technique begins with a complex problem or question, which is then broken down into smaller, more manageable sub-problems or questions. This decomposition is crucial for tackling complex issues in a systematic and methodical way.

2. **Detailed Preliminary Content**: Before addressing the main problem, the AI provides extensive preliminary content, including foundational concepts, relevant theories, and useful hints. This step ensures that all necessary background information is covered to understand and solve the problem.

3. **Step-by-Step Problem Solving**:
   
   - **Intermediate Questions**: The AI formulates a series of intermediate questions, each targeting a specific aspect of the complex problem. These questions guide the problem-solving process in a structured manner.
   
   - **Answer Sketches and Code Execution**: For each question, the AI develops a detailed answer sketch, which is then tested and refined through code execution. This process not only verifies the accuracy of the answer but also deepens the understanding of the problem.
   
   - **Detailed Answers**: Based on the code execution results, the AI provides comprehensive and detailed answers for each intermediate question, gradually building towards the solution of the original complex problem.

4. **Final Solution Presentation**:
   
   - **Solution Synthesis**: After addressing all intermediate questions, the AI synthesizes the findings into a complete solution for the original complex problem.
   
   - **Code for Final Solution**: The final solution is further verified or solved using coding, ensuring accuracy and precision.
   
   - **Formatted Final Answer**: The solution is presented in a clear, concise, and formally correct format, often using LaTeX for mathematical precision and enclosed within `\boxed{}` for emphasis.

```markdown
<syntax>

## Problem: [problem]

Solution: Let's think step by step. [somewords interpreting the origin problem]

### Preliminary Contents

- **Prelim 1**: [preliminary contents 1]
  
- **Prelim 2**: [preliminary contents 2]

- [...]

### Hints
- **Hint 1**: [useful hints 1]
  
- **Hint 2**: [useful hints 2]

- [...]

### Intermediate Steps: Question-AnswerSketch-Code-Output-Answer Pairs

Let's think step by step.

#### Question 1: [the first question you raised]
- **Answer Sketch**: [write a sketch of your answer to question 1]

##### Code Interpreter for Question 1
[call code interpreter here to verify and solve your answer sketch to question 1]

#### Answer for Question 1
- **Answer**: [your answer to this question 1 based on the results given by code interpreter (if presented)]

#### Question 2: [the second question you raised]
- **Answer Sketch**: [write a sketch of your answer to question 2]

##### Code Interpreter for Question 2
[call code interpreter here to verify and solve your answer sketch to question 2]

#### Answer for Question 2
- **Answer**: [your answer to this question 2 based on the results given by code interpreter (if presented)]

#### Question 3: [the second question you raised]
- **Answer Sketch**: [write a sketch of your answer to question 3]

##### Code Interpreter for Question 3
[call code interpreter here to verify and solve your answer sketch to question 3]

#### Answer for Question 3
- **Answer**: [your answer to this question 3 based on the results given by code interpreter (if presented)]


### [Question ...]

### Final Solution:

Recall the origin problem <MathP> [origin problem] </MathP>. 

Let's think step by step.

#### Solution Sketch
[write a sketch for your final solution]

#### Code Interpreter for Final Solution
[call code interpreter here to verify and solve your final solution]

#### Final Answer
[present the final answer in latex boxed format, e.g., $\boxed{63\pi}$]
Final Answer: the answer is $\boxed{...}$.

</syntax>
```

```xml
<system>
<description>
As one of the most distinguished mathematicians, logicians, programmers, and AI
scientists, you possess an unparalleled mastery over various mathematical domains.
You approach problems methodically, with detailed articulation and Python code execution.
</description>
<instructions>
<objective>
Automatically configure solutions to complex mathematical problems with Python code execution.
</objective>
<key_priorities>
<priority>Generate useful hints for solving the problem.</priority>
<priority>Craft intermediate questions that
break down the problem, solving them with code.</priority>
<priority>Automatically configure solutions where applicable.</priority>
</key_priorities>
<code_execution_guidelines>
<guideline>Import necessary libraries in all code blocks,
such as ’from sympy import *’.</guideline>
<guideline>Maintain variable inheritance across code blocks,
excluding blocks with errors.</guideline>
<guideline>Execute all code blocks immediately after writing to validate them.
</guideline>
</code_execution_guidelines>
<mathematical_formatting>
<format>Present the final answer in LaTeX format, enclosed within ’\boxed{}’
without units.</format>
<format>Use ’pi’ and ’Rational’ from Sympy for pi and fractions,
simplifying them without converting to decimals.</format>
</mathematical_formatting>
</instructions>
</system>
<syntax>
<problem_structure>
<problem_definition>
<!-- Insert Problem Here -->
</problem_definition>
<solution_approach>
<!-- Insert Step-by-Step Solution Approach Here -->
</solution_approach>
<preliminary_contents>
<!-- Insert Preliminary Contents Here -->
</preliminary_contents>
<hints>
<!-- Insert Useful Hints Here -->
</hints>
<intermediate_steps>
<!-- Insert Intermediate Steps (Questions, Answers, Code) Here -->
</intermediate_steps>
<final_solution>
<solution_sketch>
<!-- Insert Solution Sketch Here -->
</solution_sketch>
<code_for_solution>
<!-- Insert Code for Final Solution Here -->
</code_for_solution>
<final_answer>
<!-- Insert Final Answer Here -->
</final_answer>
</final_solution>
</problem_structure>
</syntax>
```

### Application and Use Cases:

- **Ideal for Complex Mathematical Problems**: This approach is particularly effective for solving intricate mathematical problems that require a multi-step solution process.

- **Adaptability to Other Fields**: While primarily used for mathematics, the structure can be adapted to other fields like physics, engineering, and computer science, where complex problem-solving is required.

- **Educational Tool**: In an educational context, it can help students learn how to approach and solve complex problems step by step.

This version of Meta Prompting is designed to tackle problems that are too complex to be solved in a straightforward manner. It encourages a meticulous and methodical approach, ensuring that each aspect of the problem is thoroughly understood and addressed. The use of intermediate questions and detailed answer sketches, combined with code execution, makes it an effective strategy for deep and complex reasoning.



## Citations
Please cite the paper and star this repo if you use Meta Prompting (MP) and Cumulative Reasoning (CR) and find it interesting/useful, thanks! Feel free to contact zhangyif21@tsinghua.edu.cn or open an issue if you have any questions.

```bibtex
@article{zhang2023meta,
  title={Meta Prompting for AGI Systems},
  author={Zhang, Yifan},
  journal={arXiv preprint arXiv:2311.11482},
  year={2023}
}

@article{zhang2023cumulative,
  title={Cumulative Reasoning With Large Language Models},
  author={Zhang, Yifan and Yang, Jingqin and Yuan, Yang and Yao, Andrew Chi-Chih},
  journal={arXiv preprint arXiv:2308.04371},
  year={2023}
}
```
