# Style Guide for DevOps-and-Cloud-101

To ensure consistency and readability across this repository, please follow the style guide below when contributing code, tutorials, or documentation.

## General Guidelines

- **Write clear and concise content**. Tutorials should be easy to follow, and code should be simple and efficient.
- **Be specific** in your explanations. When writing about AWS services or DevOps tools, provide detailed steps, commands, and examples.
- Use **descriptive filenames** (e.g., `linux-basics.md`, `docker-setup.md`, `aws-vpc.md`).
- Always use **markdown** for writing tutorials and documentation files.

## Naming Conventions

- **Tutorials**: Use lowercase, hyphenated names for tutorial files (e.g., `intro-to-aws.md`, `getting-started-with-docker.md`).
- **Tasks and Exercises**: Use the format `task-name.md` (e.g., `create-s3-bucket.md`, `set-up-ec2-instance.md`).
- **Example Files**: Use descriptive names for example files, e.g., `dockerfile-example.md`, `vpc-networking-example.md`.

## Code Formatting

- **Markdown Formatting**:
  - Use headers (`#`, `##`, etc.) for sections and subsections.
  - Use code blocks for commands and configuration files. Wrap shell commands in triple backticks:
    ```bash
    sudo apt update
    sudo apt install docker
    ```

- **Commands & Configurations**:
  - For shell commands, use `bash` code blocks.
  - For configuration files (e.g., YAML, JSON), use language-specific code blocks (e.g., `yaml`, `json`).

- **File Structure**:
  - Keep file structures clean and logical. Group related tutorials and tasks together within relevant directories (e.g., `DevOps/Linux/`, `AWS/EC2/`).

## Testing and Verification

- **Ensure your tutorial or task is functional**. Test any examples, code, and commands before adding them.
- If possible, include tests for your tutorial or example to verify that it works.
- Include setup instructions for each tutorial. Make sure users can easily follow the tutorial and perform all tasks with minimal setup.

## Writing Tutorials

- Each tutorial should include:
  - **Prerequisites** (e.g., tools or knowledge needed to follow the tutorial).
  - **Step-by-step instructions**, with clear code examples.
  - **Expected outcome** (what the learner will accomplish at the end).
  - **Next steps** (optional suggestions for further learning).
