[Watch the full setup walkthrough on YouTube](https://www.youtube-transcript.io/videos?id=QwEjsQOQyhQ)

## Your First Python Program ("Hello, World!")

This chapter guides you through creating and running your very first Python script. This is a fundamental step to verify that your environment is set up correctly and to get you comfortable with the basic workflow of coding.

### 1. Create a Project Folder

Inside your cloned `code-blossom-applied-ai` repository, create a new folder to keep your Python practice files organized. In the session, we named it `python-onboarding`.

### 2. Create a New Python File

-   Inside your new folder, create a file named `hello_world.py`.
-   The `.py` extension is crucial as it tells VS Code and the Python interpreter that this is a Python file.

### 3. Write The Code

You can use an AI assistant like ChatGPT or the open-source alternative shown in the session to generate the code. This is a great way to start leveraging AI in your workflow!

Ask the AI: **"Create a Python program that says hello world"**

It will generate a simple line of code. Copy and paste it into your `hello_world.py` file:

```python
# This line prints the string "Hello, world!" to the console.
print("Hello, world!")
```

### 4. Open the VS Code Terminal

In VS Code, you can open an integrated terminal by going to the top menu and selecting `Terminal` > `New Terminal`. This is where you will run your code.

### 5. Run Your Program

First, you need to navigate into the folder where you created your file. Use the `cd` (change directory) command:

```bash
# Replace 'python-onboarding' with your folder name if it's different
cd python-onboarding
```

Now, execute your script using the `python` command:

```bash
python hello_world.py
```

If everything is set up correctly, you will see the following output in your terminal:

```
Hello, world!
```

**Congratulations! You've just run your first Python program.**

### Full Module Content

---

### **Week 1: Development Environment Setup**

#### **1. Core Tools Installation**

**Goal:** Install the essential software required for this course.

*   **Python:** The core programming language we will use.
    *   **Action:** Download and install the latest version of Python from the official website.
    *   **Resource:** [Python Downloads](https://www.python.org/downloads/)
*   **Visual Studio Code (VS Code):** A powerful and popular code editor (also called an IDE - Integrated Development Environment).
    *   **Action:** Download and install VS Code.
    *   **Resource:** [VS Code Download](https://code.visualstudio.com/download)
*   **Git:** A version control system to track changes in your code and collaborate with others.
    *   **Action:** Download and install Git.
    *   **Resource:** [Git Downloads](https://git-scm.com/downloads)
*   **Node.js and NPM:** NPM (Node Package Manager) was mentioned for future web development projects (e.g., React frontends for your AI models). It's good to install it now.
    *   **Action:** Download and install Node.js (NPM is included).
    *   **Resource:** [Node.js Downloads](https://nodejs.org/)

---

#### **2. Setting Up The Project with Git & GitHub**

**Goal:** Get a copy of the class project from GitHub onto your computer.

*   **GitHub:** A web platform that hosts Git repositories. We use it to share code and track tasks.
*   **Cloning:** "Cloning" is the process of creating a local copy of a remote repository on your computer.
*   **Actions:**
    1.  Accept the GitHub collaborator invitation sent to your email.
    2.  Open VS Code.
    3.  From the welcome screen, select "Clone Git Repository."
    4.  Paste the repository URL provided in the chat: `https://github.com/good-company/code-blossom-applied-ai`
    5.  Choose a location on your computer to save the project.
    6.  Open the cloned repository.

---

#### **3. Your First Python Program ("Hello, World!")**

**Goal:** Write and execute a simple Python script to confirm your setup works.

*   **Actions:**
    1.  In VS Code, create a new folder (e.g., `python-onboarding`) and a new file inside it named `hello_world.py`.
    2.  Add the following code to the file: `print("Hello, world!")`
    3.  Open a new terminal in VS Code (`Terminal` > `New Terminal`).
    4.  Navigate into your folder: `cd python-onboarding`
    5.  Run the script: `python hello_world.py`
    6.  You should see "Hello, world!" printed in the terminal.

---

#### **4. Basic Git Workflow & Collaboration**

**Goal:** Learn how to save your work and get updates from others using Git.

*   `git pull`: Gets the latest changes from the GitHub repository. **Always do this before you start working.**
    ```bash
    git pull
    ```
*   `git status`: Shows you which files you have changed.
*   `git add`: Stages your changes, preparing them to be saved.
    ```bash
    # Stage a specific file
    git add hello_world.py

    # Stage all changed files
    git add .
    ```
*   `git commit`: Saves your staged changes to your local repository with a descriptive message.
    ```bash
    git commit -m "feat: Add hello world program"
    ```
*   `git push`: Pushes your committed changes from your local machine to the remote GitHub repository so others can see them.
    ```bash
    git push
    ```

---

#### **5. Troubleshooting Common Setup Issues**

**Goal:** Learn how to solve common problems you might encounter during setup.

*   **Problem:** `python` or `git` command not recognized in the terminal.
    *   **Cause:** The tool was installed, but your system's `PATH` environment variable wasn't updated. The `PATH` tells the terminal where to find executable programs.
    *   **Solution:** Re-install Python or Git, making sure to check the box that says **"Add Python to PATH"** or **"Add to PATH"** during the installation process.
*   **Problem:** Slow computer performance.
    *   **Cause:** Low disk space, too many background processes, or visual effects.
    *   **Solution:**
        1.  **Free up disk space:** Run the "Disk Cleanup" utility on your C: drive, as shown in the session.
        2.  **Improve performance:** Disable Windows visual effects by running `sysdm.cpl` and choosing "Adjust for best performance."
        3.  **Close unnecessary applications:** Shut down programs you aren't using to free up memory (RAM).
*   **Understanding `import sys`:** In the session, we explored how to find where Python is installed. The `sys` module provides access to system-specific parameters and functions. [altcademy.com](https://www.altcademy.com/blog/what-is-import-sys-in-python/)
    ```python
    # This code, when run in a Python console, shows where Python looks for modules.
    import sys
    print(sys.path)
    ```
*   **Further Learning:** For a deep dive into how Python imports modules and uses `sys.path`, this tutorial is excellent:
    *   **Video:** [Corey Schafer - Import Modules and The Standard Library](https://www.youtube.com/watch?v=CqvZ3vGoGs0) ([youtube.com](https://www.youtube.com/watch?v=CqvZ3vGoGs0&t=638s))
```