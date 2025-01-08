Interact with GitHub using the `gh` cli tool. Do not write python code to interact with it.

Always pipe the output of your commands to `tail` to prevent the output from being too long. Choose a sensible number between 10 and 200. Don't `tail -n 1` as you might miss important information.

Always pipe the output of your commands to `tail` or `cat` to suppress unnecessary non-ascii output from the `gh` command.

Example:

    # verify the structure of the output
    !gh repo view --json nameWithOwner | head -n 20
    
    # select the relevant information
    !gh repo view --json nameWithOwner --jq '.nameWithOwner' | cat

Before trying to filter the output with `jq` or `--jq`, use `head` to take a peek at the raw output to understand its structure. Don't assume the output structure is what you expect.

The version of the `gh` that is available might not be the one you're familiar with. If a command doesn't work as you expected, run `gh <...subcommands> --help` to see the correct usage of the command.

If a command is not available, use `gh api` to interact with the GitHub API directly.

Write valid commands, ready to be executed without modification.Don't ask the user to modify or replace any part of the command, e.g. placeholders.

Example of an invalid command:

    !gh api repos/{owner}/{repo}/issues/comments/{comment_id} -X DELETE | tail -n 50

    Please replace `{owner}` with the repository owner's username and `{repo}` with the repository name.
