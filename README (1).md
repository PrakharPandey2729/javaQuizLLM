# Java MCQ Generator with Evaluator Workflow

This project generates multiple-choice questions (MCQs) based on Java programming topics, evaluates the quality and trickiness of the questions, and ensures alignment with a provided syllabus. It uses a state graph workflow to iteratively refine questions and execute Java code to verify the correct answers.

---

## Features

- **Question Generation:** Generates tricky Java MCQs from various topics.
- **Evaluator Nodes:** Includes syllabus and trickiness evaluators to refine the questions iteratively.
- **Java Code Execution:** Compiles and runs the Java code to ensure correctness of answers.
- **Interactive Refinement:** Allows multiple revisions based on feedback from evaluators.

---

## Prerequisites

1. **Python**: Version 3.7 or higher.
2. **Java**: Ensure Java is installed and accessible via the command line (`javac` and `java` commands).
3. **Python Dependencies**: Install the required Python packages listed below.

---

## Setup

###  Clone the Repository

```bash
git clone https://github.com/HarshRathi2511/java-quiz-gen-bot.git
cd java-quiz-gen-bot
```

###  Set Up API Key

The project uses OpenAI's API for generating and refining questions. You need to set your OpenAI API key in the `config.py` file. Replace the placeholder `open_api_key` with your actual OpenAI API key:

```python
# config.py

open_api_key = "sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
```

If you don't have an API key, sign up at [OpenAI](https://platform.openai.com/) to obtain one.

---

## Usage

1. Run the script using the Run all in the notebook

2. The program will execute the state graph workflow, starting with question generation and proceeding through syllabus and trickiness evaluation.

3. The final output includes:
   - The Java MCQ code, properly formatted.
   - Answer options with the correct answer determined via Java code execution.

4. Outputs are displayed directly in the terminal with syntax highlighting for the Java code.

---

## Example Workflow

1. The system generates an initial Java MCQ question.
2. Evaluators review the question:
   - **Syllabus Evaluator** ensures alignment with the Java syllabus.
   - **Trickiness Evaluator** increases complexity if necessary.
3. Feedback is aggregated and used to refine the question.
4. The Java code is compiled and executed to verify the output, ensuring the correct answer aligns with one of the provided options.

---

## Notes

- Ensure your system has `javac` and `java` commands accessible in the system's `PATH`.
- Adjust the `max_revisions` parameter in the script to control the number of refinement iterations.
- Check the final question and options for formatting or additional modifications if required.

---

## Troubleshooting

### Common Issues

1. **Java Not Found**: Ensure Java is installed and properly added to your system's PATH.
2. **API Key Error**: Verify your OpenAI API key is correctly set and active.

---

## Contributing

Feel free to fork the repository and submit pull requests for any enhancements or bug fixes. For major changes, please open an issue first to discuss what you would like to change.

---

Happy Coding! 🎉