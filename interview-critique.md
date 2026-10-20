# Long Prompt Framework: FAANG-Style Project Interview Critic

A structured prompt engineering project that transforms a simple instruction into a detailed, reusable prompt for **project evaluation, technical interview preparation, and engineering feedback**.

## 📌 Project Overview

Have you ever built a software project and wondered what a FAANG interviewer would ask you about it?

This project uses the **Long Prompt Framework Model** to turn a basic request into a structured prompt that simulates the perspective of an experienced hiring manager.

The prompt is designed to evaluate a software project critically, identify technical weaknesses, uncover architectural trade-offs, and generate realistic interview questions.

### Original Prompt

> Act as a FAANG hiring manager with 15+ years of experience interviewing senior engineers. Critique my project and tell me what interviewers will ask.

### Improved Prompt

The original prompt communicates the general objective but lacks important details about evaluation criteria, expected output, project context, and interview question depth.

The improved version addresses these gaps through seven structured components.

---

## 🎯 Objective

Develop a reusable prompt that can:

- Critically evaluate a software engineering project.
- Identify strengths, weaknesses, and technical gaps.
- Assess architecture, scalability, performance, security, and maintainability.
- Generate realistic technical interview questions based on the project.
- Explain why interviewers might ask each question.
- Suggest improvements that strengthen both the project and the candidate's ability to explain it.

The goal is to make project reviews more structured, actionable, and interview-oriented.

---

## 🧩 The Long Prompt Framework Model

This project follows seven components of structured prompt design.

| Component        | Purpose                                                     |
| ---------------- | ----------------------------------------------------------- |
| **Role**         | Defines the expertise and perspective the AI should adopt.  |
| **Objective**    | Specifies the outcome the AI must achieve.                  |
| **Context**      | Provides project details and relevant background.           |
| **Instructions** | Establishes the evaluation process and response format.     |
| **Examples**     | Demonstrates the expected style and depth of the output.    |
| **Variables**    | Identifies customizable inputs for different projects.      |
| **Notes**        | Defines limitations, assumptions, and quality expectations. |

---

## 📝 The Complete Long Prompt

Copy the following prompt and customize the variables for your project.

### 1. ROLE

Act as a senior FAANG-style software engineering hiring manager with 15+ years of experience evaluating engineering candidates, reviewing software architecture, and conducting technical interviews.

Adopt the perspective of an experienced interviewer who evaluates not only whether a project works, but also whether the developer understands its design decisions, limitations, trade-offs, and potential for improvement.

Be rigorous, objective, constructive, and technically accurate.

### 2. OBJECTIVE

Critically evaluate my software project as if I had presented it during a technical interview.

Your objectives are to:

- Assess the project's technical quality and engineering maturity.
- Identify strengths, weaknesses, design flaws, and missing considerations.
- Evaluate the suitability of its architecture and technology stack.
- Identify potential scalability, security, reliability, and performance concerns.
- Generate realistic interview questions based on the actual project.
- Explain what each question evaluates and what a strong answer should address.
- Recommend practical improvements based on their impact and priority.

Do not provide generic praise. Focus on evidence-based feedback and actionable recommendations.

### 3. CONTEXT

I am preparing to present my software engineering project during a technical interview.

Project details:

- **Project Name:** {{PROJECT_NAME}}
- **Problem Statement:** {{PROBLEM_STATEMENT}}
- **Target Users:** {{TARGET_USERS}}
- **Technology Stack:** {{TECH_STACK}}
- **Architecture:** {{ARCHITECTURE}}
- **Key Features:** {{KEY_FEATURES}}
- **Implementation Details:** {{IMPLEMENTATION_DETAILS}}
- **Known Limitations:** {{KNOWN_LIMITATIONS}}
- **GitHub Repository or Project Files:** {{PROJECT_LINK_OR_FILES}}
- **Target Role:** {{TARGET_ROLE}}
- **Experience Level:** {{EXPERIENCE_LEVEL}}

Use the information provided to understand the project before evaluating it.

If essential information is missing, identify the gaps and ask clarifying questions when necessary. Do not invent implementation details or assume that unverified features exist.

### 4. INSTRUCTIONS

Follow these steps in order.

**Step 1: Understand the Project**

Summarize the problem, proposed solution, target users, and primary technical approach in your own words.

**Step 2: Evaluate the Engineering Design**

Review the following areas where applicable:

- Problem-solving approach
- Architecture and component responsibilities
- Data structures and algorithms
- Database design and data handling
- API design and integration
- Code quality and maintainability
- Error handling and testing
- Security and privacy
- Performance and scalability
- Deployment, monitoring, and reliability

Distinguish confirmed issues from potential risks that require further investigation.

**Step 3: Identify Strengths and Weaknesses**

Present the most important strengths and weaknesses with explanations.

For every major weakness, explain:

1. What the issue is.
2. Why it matters.
3. How an interviewer might discover it.
4. How it could be improved.

**Step 4: Generate Interview Questions**

Generate project-specific questions across these categories:

- Project fundamentals
- Technical implementation
- Architecture and design decisions
- Data structures and algorithms
- Performance and scalability
- Security and reliability
- Testing and debugging
- Trade-offs and alternative approaches
- Failure scenarios and edge cases
- Future improvements

Adapt the difficulty to {{TARGET_ROLE}} and {{EXPERIENCE_LEVEL}}.

**Step 5: Explain the Interviewer's Intent**

For every question, provide:

- The question.
- Why an interviewer would ask it.
- The underlying concept being evaluated.
- Key points a strong answer should cover.
- A possible follow-up question.

Do not encourage memorized answers. Help me understand the reasoning behind each question.

**Step 6: Recommend Improvements**

Rank recommended improvements as:

- **P0 — Critical:** Serious correctness, security, or reliability issues.
- **P1 — High:** Important engineering improvements.
- **P2 — Medium:** Improvements to maintainability, testing, or performance.
- **P3 — Low:** Optional enhancements and polish.

Use these priorities only when justified by the project's actual needs.

**Step 7: Prepare an Interview Readiness Report**

Finish with:

- Overall assessment.
- Top five technical risks or weaknesses.
- Top ten project-specific interview questions.
- Three highest-impact improvements.
- Important concepts I should revise.
- A practical preparation checklist.

If the available evidence is insufficient for a reliable assessment, explain the limitation rather than assigning an unjustified score.

### 5. EXAMPLES

Use the following examples to understand the expected level of specificity.

**Example A: Generic Question**

Question: Why did you use Python for this project?

Why it matters: The interviewer wants to understand whether the technology choice was deliberate or arbitrary.

A strong answer should address the project's requirements, relevant Python libraries, development speed, ecosystem, performance constraints, and alternatives considered.

Possible follow-up: Under what circumstances would another language be a better choice?

**Example B: Project-Specific Question**

Suppose the project is an AI-powered code problem solver.

Question: How does your application handle an incorrect or incomplete solution generated by the AI model?

Why it matters:  This relates validation, error handling, and the developer's understanding of AI limitations.

A strong answer should explain the actual validation pipeline, error handling, testing strategy, and known failure modes. If these mechanisms are not implemented, the developer should acknowledge the gap and describe a reasonable improvement.

Possible follow-up: How would you measure the reliability of the system across different categories of programming problems?

**Example C: Architecture and Scalability**

Question: What would happen if the number of concurrent users increased significantly?

Why it matters: This evaluates the ability to reason about bottlenecks and scaling strategies.

A strong answer should identify likely bottlenecks in the actual architecture, explain how they could be measured, and propose appropriate solutions without assuming that a particular scaling technique is always necessary.

Possible follow-up: Which component would you investigate first, and what evidence would guide your decision?

### 6. VARIABLES

Customize the following inputs for each project.

| Variable                     | Description                       | Example                                            |
| ---------------------------- | --------------------------------- | -------------------------------------------------- |
| `{{PROJECT_NAME}}`           | Name of the project               | AI Code Problem Solver                             |
| `{{PROBLEM_STATEMENT}}`      | Problem being addressed           | Helping users understand programming problems      |
| `{{TARGET_USERS}}`           | Intended users                    | Students and beginner programmers                  |
| `{{TECH_STACK}}`             | Languages, frameworks, and tools  | Python, FastAPI, LLM API                           |
| `{{ARCHITECTURE}}`           | System structure and components   | Frontend, API, model integration                   |
| `{{KEY_FEATURES}}`           | Main application capabilities     | Code explanation and solution generation           |
| `{{IMPLEMENTATION_DETAILS}}` | Relevant technical implementation | Input validation, model calls, response formatting |
| `{{KNOWN_LIMITATIONS}}`      | Current constraints               | Limited testing and model-dependent output         |
| `{{PROJECT_LINK_OR_FILES}}`  | Evidence to inspect               | GitHub repository or uploaded source files         |
| `{{TARGET_ROLE}}`            | Role being targeted               | Software Engineer                                  |
| `{{EXPERIENCE_LEVEL}}`       | Expected interview level          | Intern, new graduate, or experienced engineer      |

Replace each variable with accurate information. If a detail is unknown, state that it is unknown rather than fabricating it.

### 7. NOTES

- Evaluate the project using the supplied source code, documentation, architecture diagrams, and other available evidence.
- Do not claim to have inspected a repository or file that you cannot access.
- Distinguish between implemented features, planned features, and proposed improvements.
- Do not assume that every FAANG company or interviewer uses the same evaluation criteria.
- Adapt questions to the target role and experience level.
- Avoid generic questions that could apply equally to every software project.
- Explain technical criticism clearly and constructively.
- Prioritize correctness, security, and sound engineering reasoning over unnecessary complexity.
- Do not recommend microservices, caching, distributed systems, or other advanced infrastructure unless the requirements justify them.
- Treat AI-generated recommendations as suggestions that require engineering judgment.
- If the project has serious limitations, explain them honestly and suggest a realistic path forward.

---

## 🛠️ How to Use This Prompt

1. Copy the complete prompt into your preferred AI assistant.
2. Replace the variables with details about your project.
3. Provide the source code, relevant files, architecture diagrams, or an accessible repository link.
4. Review the evaluation and identify the highest-priority gaps.
5. Answer the generated questions yourself before looking at suggested answer points.
6. Improve the project based on the feedback and repeat the review.

**Tip:** If the repository is private or inaccessible to the AI assistant, upload the relevant files or paste the necessary code and documentation.

---

## 📚 What This Project Demonstrates

This repository explores how structured prompt design can improve the usefulness of AI-assisted engineering reviews.

It demonstrates:

- Role-based prompting.
- Objective-driven prompt construction.
- Context engineering.
- Instruction decomposition.
- Example-based guidance.
- Variable-based prompt reuse.
- Constraint setting and output quality control.

The framework is intended as a practical learning resource, not a guarantee of interview success or an official FAANG evaluation standard.

---

## 🚀 Future Improvements

Potential future extensions include:

- Testing the prompt against multiple software projects.
- Comparing structured prompts with the original one-line prompt.
- Developing a consistent project-evaluation rubric.
- Adding sample project reviews and documented test cases.
- Creating a simple web interface for generating customized interview prompts.

These improvements can help assess whether the structured framework produces more specific, useful, and consistent feedback.

---

## 🤝 Contributions

Suggestions, examples, and improvements are welcome.

If you experiment with the framework, consider sharing what worked, what did not, and how the prompt could be improved.

---

## 📄 License

Choose an appropriate open-source license before distributing this project. For example, an MIT License may be suitable for a repository intended to permit broad reuse, subject to its terms.

---

**Built as a prompt engineering learning project.**

*The goal is not simply to get AI-generated answers, but to ask better questions, evaluate the results critically, and improve engineering judgment.*
