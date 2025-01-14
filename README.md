# 2025-01-14 DSCI 310

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
