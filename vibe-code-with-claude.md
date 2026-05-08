# How I Vibe Code with Claude

I use Claude as a coding partner to accelerate development, reduce repetitive or boring work, and help me stay in flow longer.

## Preparation
- [VS Code](https://code.visualstudio.com/)
- [Claude CLI](https://code.claude.com/docs/en/overview#get-started)
- [Claude Code for VS Code](https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code)
- [Git](https://git-scm.com/install/)

## Workflow

In this example, the process begins with building a desktop app called **Todo App** with Wails. First, set up the project directory and initialize it as a Git repository to ensure version control is active from the very first line of code.

```shell
mkdir todo-app
cd todo-app
git init
```

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/71be3658-e648-4457-821f-eef15bfee65c" />

<br />

Open the newly created project in Visual Studio Code to begin the development process.

```shell
code .
```

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/a9056d7c-a527-479f-ba2f-f25c105322f9" />

<br />

Before touching the code, create a `PRD.md` (Product Requirements Document). This serves as the "source of truth" and provides Claude with the necessary context regarding the app's features and constraints.

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/840d4f39-dde9-4f5d-8ea5-54627e12dbd2" />

<br />

To start the vibe coding session, open the Claude Chat panel via the VS Code Command Palette by pressing `Ctrl + Shift + P` (Windows/Linux) or `Cmd + Shift + P` (macOS), then typing **"Claude Code: Open in Side Bar"** and hitting **Enter**. 

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/ca925201-1781-40dc-9ec2-0a3c4a310660" />

<br />

Now you're ready to turn that PRD into a functional application while letting the vibes and code flow.

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/96b18d12-41d7-470b-96c0-42ef5116f39e" />

<br />

To generate the PRD, input a detailed prompt that defines the "todo-app" as a minimalist desktop application built with Wails (Go + Vue). This prompt ensures the document covers everything from product goals and core features—like the sticky-note-style floating widget—to technical architecture and data models, focusing on a clean, low-distraction native desktop experience.

```markdown
Create a complete "PRD.md" for a minimalist desktop application called "todo-app" built with Wails (Go + Vue).
The app is an offline-first sticky-note-style todo widget that floats on the desktop and automatically shows today's tasks by default.
Users can expand the widget into a larger window to view and manage todos from other dates.
The PRD should cover the product overview, goals, core features, UX behavior, floating widget behavior, local storage, technical architecture, folder structure, data models, keyboard shortcuts, MVP scope, and future improvements.
Focus on simplicity, fast performance, clean modern UI, low distraction, and a native desktop experience across Windows, macOS, and Linux.
```

<img width="1440" height="900" alt="Generate PRD Prompt" src="https://github.com/user-attachments/assets/4fefe705-6ea8-4556-9466-9f40d32b6b44" />

<br />

Once the PRD is generated, it is essential to commit the changes to Git. This practice ensures your progress is saved and provides a clear history of the project's foundational requirements.

<img width="1440" height="900" alt="Commit to Git" src="https://github.com/user-attachments/assets/8ea11c93-49b0-47c8-88b2-20f64b7c0292" />

<br />

Next, break the PRD down into manageable development tasks by creating a `TASKS.md` file. Using a specific prompt allows Claude to generate implementation-focused tasks with checkboxes, clear definitions of done, and specific constraints to help track development progress efficiently.

```markdown
Based on "PRD.md", generate "TASKS.md" that breaks the project into clear, implementation-focused dev tasks.
Each task should use markdown checkboxes so progress can be tracked easily.
Every task must clearly explain what needs to be built, the expected result/output, important implementation details or constraints, or the definition of done.
```

<img width="1440" height="900" alt="Generate Tasks" src="https://github.com/user-attachments/assets/a89475d8-e9ea-492a-8e1c-8c3affcd02bd" />

<br />

Remember to commit your changes once more after the task breakdown is complete to maintain a clean and tracked project history.

<img width="1440" height="900" alt="Commit Task Breakdown" src="https://github.com/user-attachments/assets/61539c57-8410-4df2-b9c5-9b3adcd8714b" />

<br />

With the task list finalized, you can begin executing them one by one until the project is finished. Use the following prompt template to guide Claude through each task, ensuring consistency and adherence to your requirements:

> Based on "TASKS.md", implement task "<TASK_NAME>" from "<PHASE_NAME>". Read the task requirements carefully and follow all defined constraints exactly as written. Ensure the implementation is clean, production-ready, and aligned with the architecture and conventions defined in "PRD.md". After completing the task, update "TASKS.md" by marking the checkbox as completed while preserving the existing formatting and structure.

Simply replace `<TASK_NAME>` and `<PHASE_NAME>` with the specific task and phase you are currently working on. Here is a concrete example for the very first task:

```text
Based on "TASKS.md", implement task "T-001 · Initialize Wails project" from "Phase 0 — Project Bootstrap".
Read the task requirements carefully and follow all defined constraints exactly as written.
Ensure the implementation is clean, production-ready, and aligned with the architecture and conventions defined in "PRD.md".
After completing the task, update "TASKS.md" by marking the checkbox as completed while preserving the existing formatting and structure.
```

<img width="1440" height="900" alt="Execute First Task" src="https://github.com/user-attachments/assets/048f5206-4f5c-4f7f-b860-f89b5c5ade14" />

<br />

Once Claude completes the assigned task, it's time to commit the changes. A recommended practice is to use a consistent commit message format, such as `feat: <TASK_NAME>`, to keep the project history organized.

<img width="1440" height="900" alt="Commit First Task" src="https://github.com/user-attachments/assets/d78bdb28-e5f7-4b31-a188-fd0a46f1d65d" />

<br />

From here, proceed to complete all remaining tasks in the list. Ensure you commit and push regularly to keep your code safely stored and easily trackable.

You can find the repository for this guide at the following link: [https://github.com/iqbaleff214/todo-app-desktop](https://github.com/iqbaleff214/todo-app-desktop). 
