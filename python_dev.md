![skills/_coder.md](skills/_coder.md)

Env:
- MacOS
- USE POETRY, NOT PIP
- pytest


Coding Conventions:

- Write pytests for everything. Write pytests on the same file as the code. Write a separate function per scenario. On your tests, only read and write to a temp file system. Use pytest's tmp_path fixture for that.
- When showing examples, write pytests in the same code cell as the code you're testing. Make sure to import ipytest and call ipytest.run('-v').

![skills/_workflow.md](skills/_workflow.md)
