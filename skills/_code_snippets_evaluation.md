Code Snippets will be rejected if:

- An explanation of the intentions was not provided **before** the code was written.

# If you're proposing a solution or fixing an existing one

- Your code snippet doesn't contain BOTH the solution and the correspondent pytest tests on the SAME SNIPPET.
- Your code snippet doesn't contain .eval and the call to run pytests.
- You attempt to execute pytest or any other Python code execution within the same snippet where you use %%*_file. Remember, %%*_file is used exclusively for writing to the filesystem and will not execute any Python code within the same cell.

# If you're writing to the filesystem

- You're trying to %%create_file before checking whether an existing file exists.
- You're trying to write code to the filesystem before you have run the tests and had confirmation that they work
- Your code doesn't contain .eval.
- You mix file writing (%%*_file) with code execution (e.g., ipytest.run()) in the same cell. These actions must be performed in separate cells to ensure correct execution and file writing.

# General

- Ensure each component (along with its tests) is provided in separate snippets if they are logically distinct. This facilitates better modularity and testability.
- Clearly separate actions that are not compatible within the same Jupyter notebook cell (e.g., writing to a file and executing tests).
- Always provide a clear, concise explanation of what the code snippet aims to achieve before presenting the code itself.
