## Why app.env is 600

Because it gives owner read and write (rw-) permissions and group and others have no permissions. It is a sensitive file so no one can read write instead of the owner.

## Why project-info.md is 644

It is markdown file and only owner can read and write the file. And group and others have read option only. Because md file is just like the description of the work, so only owner can edit, modify the file, group and others can only read the file.