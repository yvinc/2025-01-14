# 2025-01-14 DSCI 310

### Resolving Merge Conflicts and Creating Empty Folder

-   yayyy

-   advil

-   🥸

    ## Note:

    -   Pull first before push!

        -   Git is sensitive to merge conflicts.

        -   Occurs when: Changes made simultaneously on local and remote file on the **SAME** line, and you try to push the update from local onto the remote.

            -   Big scary red block of error message!

            -   Tells you to 'git pull' before pushing again:

        -   Then we run `git pull origin main`.

            -   Then we will encounter a new error message with some hit as to how to proceed next:

        -   Next step is that, we need to merge the two 'histories' into one proper history:

            -   run `git config pull.rebase false` (the first hint given by the error message after `git pull`.

            -   then We go and run git pull origin main again, after `git config`.

            -   The message tells you that it goes into an '**auto-merging**' process for the process, trying to stick everything together.

            -   The **ONLY** time this auto-merging process would **stop** and **fail** is when the changes were made on the same line of the same location.

        -   The local file will reflect the change or you can call `nano README.md` (i.e., on VScode), for example to see the both conflicting histories.

            -   Then you need to manually choose and fix the file [or]{.underline} (if working on VS code) click 'accept current change' or other 'accept' options to resolve the conflict.

                -   Delete all the extra '===' lines and markers.

        -   Then save the fixed file & run `git status`.

            -   `git status` will tell you to use `git add <file>` to resolve the conflict.

            -   Then use `git commit -m` to conclude the merge!

            -   Finally, we `git push origin main`!

            -   Case closed!

            -   🐈‍⬛

    -   When something is generated by the code, you typically don't have to worry about the code output with Git version control.

        -   On MacOS, you'd see `.DS_Store folder` that store information on whether you want to see the folder to appear when you look at the folder in `finder`.

        -   Seeing this `.DS_Store` is not a bug or an error. You can ignore this system file :p

            -   Other checkpoint / backup files can also be ignored because they have nothing to do with the code base.

    -   `code .gitignore`:

        -   The `.gitignore` file:

        -   The starting point of the folder is `.DS_store`.

        -   If you add the `.DS_store` name into the `.gitignore` file, and then if you then run `git status`, we'd no longer see the `.DS_store` file shown on the status output in the terminal.

        -   Then you add, commit, and push the edited `.gitignore` file.

    -   `mkdir`

        -   A command that makes a new folder:

            -   e.g., `mkdir img`

                -   We create a new `img` folder.

            -   [**HOWEVER**]{.underline}: If you have an empty folder, git status doesn't track it, and you wouldn't be able to confidently add and commit any subsequent changes you make inside this folder.

        -   **Solutions**:

            -   (1) Make a README.md into new `img` folder.

            -   (2) use `touch img/.gitkeep`

                -   `.gitkeep` file is a convention to tell git that you intend to keep this empty folder.

                    -   Sort of like in a textbook where you'd see a page that says: This page is intended to be left blank.

                    -   `.gitkeep` essentially update the current timestamp to the new folder.

                -   Then if you run `git status`, you will see the new folder appeared in the status message as: `img/`.

                -   Then you can `git add img/`, `commit`, and `push` as usual!

    -   To look at history on our local computer:

        -   We can run `git log`:

            -   Shows you all the commits you had!

            -   j-scrolling up.

            -   k-scrolling down.

            -   You're being put in a terminal program called '**LESS**', where you can't type any new command.

        -   To exit this log in order to type new commands, hit [**letter Q**]{.underline} on your keyboard to quit!

            -   Or you can quit the entire terminal and reopen to cd into your previous folder location again :p

        -   In `git log`

            -   The first line is the '[**`commit hash`**]{.underline}' that identify the unique commit.

                -   Repository-specific and computer-unique.

            -   Second line tells you the 'HEAD', which is the state of the project is on your computer right now.

                -   [**HEAD**]{.underline} is a marker of where exactly you are in the entire log timeline!

                -   The state is defined by the 'commit hash' (first line).

                -   **`main`** tells you of the branches avaliable to you in the project, the main branch is what's avaliable to you.

                -   `origin/main` and `origin/HEAD` tells your computer where Github is right now.

        -   If you run `git log –-oneline:`

            -   `--oneline` **is a flag that modifies the output of the command**.

            -   Tells us where we are at `HEAD`.

            -   You can see all shortened commit hash in the left side of the output.

            -   `commits` are there FOREVER!
