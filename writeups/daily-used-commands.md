1. echo: Used to print text or variables to the terminal. It is commonly used for displaying messages or piping output into files (e.g., echo "Hello" > file.txt).
2. whoami: Displays the name of the currently logged-in user. This is a quick way to verify which account you are using in the terminal.
3. id: Shows user and group information for the current user (or a specified user).

    UID: User ID (numerical identifier for the user).
    GID: Group ID (numerical identifier for the primary group).
    Groups: Lists all groups the user belongs to (e.g., sudo, which grants administrative privileges).

id -un: A specific usage of the id command.

    -u (or --user): Prints only the effective user ID (or the username).
    -n (or --name): Used with -u or -g to print the name instead of the numerical ID.
    Result: Returns just your username as a clean string, which is very useful for scripting.
