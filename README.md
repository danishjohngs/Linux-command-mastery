# Linux Command Mastery Challenge

**DevOps & Cloud Engineering | Week 1 Revision Machine Test**

## 📌 About This Project

This repository documents my hands-on practice of Linux fundamentals as part of my DevOps and Cloud Engineering learning journey.

The objective is to develop practical command-line skills, understand Linux file and directory management, manage permissions, inspect processes, investigate services and logs, and build a foundation for real-world DevOps troubleshooting.

## 🎯 Learning Objectives

- Understand the Linux filesystem hierarchy and directory navigation.
- Create, organize, copy, move, and remove files and directories.
- Read and edit files using common Linux tools.
- Understand Linux users, groups, ownership, and permissions.
- Monitor processes and terminate selected processes safely.
- Investigate system services and system logs.
- Use essential Linux commands confidently in troubleshooting workflows.
- Apply appropriate permissions to configuration files, scripts, and logs.

## 🛠️ Environment

| Component | Details |
|---|---|
| Operating System | Linux / Ubuntu / WSL |
| Terminal | Bash |
| Editor | Visual Studio Code |
| Version Control | Git |
| Repository Hosting | GitHub |
| Learning Focus | Linux Fundamentals, DevOps & Cloud Engineering |

*The exact commands and outputs may vary depending on the Linux distribution and environment.*

## 📂 Project Structure

The following structure is created during the challenge:

```text
DevOps-Lab/
├── projects/
│   ├── app.js
│   ├── index.html
│   └── project-info.md
├── backups/
│   ├── app.js.backup
│   └── app.env.backup
├── configs/
│   ├── app.env
│   └── nginx.conf
├── scripts/
│   └── docker-compose.yml
├── logs/
└── temp/
```

The bonus task uses a separate production application structure:

```text
Production-App/
├── app/
│   └── server.js
├── logs/
│   └── app.log
├── configs/
│   └── prod.env
└── scripts/
    └── deploy.sh
```

*The final structure may differ slightly depending on the required file moves and the commands executed.*

## 🧪 Tasks Completed

### Task 1 — Build Training Environment

Created the required directories using Linux directory-management commands and verified the structure.

**Commands practiced:** `mkdir`, `ls`, `ls -la`, `find`

### Task 2 — Navigation Challenge

Practiced moving between directories and identifying the current, parent, home, and root directories.

**Commands practiced:** `pwd`, `cd`

### Task 3 — Create Project Files

Created application files, configuration files, and project documentation.

**Commands practiced:** `touch`, `mkdir`, `ls`

### Task 4 — Copy & Backup Operations

Created backup copies of application and configuration files inside the backups directory.

**Commands practiced:** `cp`, `ls -la`

### Task 5 — Move & Organize

Moved `docker-compose.yml` into the scripts directory and renamed `README.md` to `project-info.md`.

**Commands practiced:** `mv`, `ls`

### Task 6 — File Content Challenge

Added environment variables and project documentation, then displayed their contents.

**Commands practiced:** `cat`, `nano`

### Task 7 — Permissions Challenge

Applied the specified Linux permissions:

| File or Directory | Permission | Meaning |
|---|---|---|
| `app.env` | `600` | Owner can read and write; group and others have no permissions |
| `scripts/` | `755` | Owner has full permissions; group and others have read and execute permissions |
| `project-info.md` | `644` | Owner can read and write; group and others can read |

**Commands practiced:** `chmod`, `ls -l`

**Security explanation:**

- **`600` for `app.env`:** Restricts access because environment files may contain passwords, API keys, tokens, or other sensitive configuration.
- **`644` for `project-info.md`:** Allows the owner to edit documentation while allowing other users to read it.
- **`755` for `scripts/`:** Allows the owner to modify the directory and permits users to access or traverse it, subject to other filesystem permissions.

### Task 8 — User Information Challenge

Inspected the current user's identity, numeric identifiers, and group memberships.

**Commands practiced:** `whoami`, `id`, `groups`

### Task 9 — Process Monitoring Challenge

Started a `sleep` process, located its process ID, terminated the selected process, and verified that it stopped.

**Commands practiced:** `sleep`, `ps aux`, `grep`, `kill`

### Task 10 — Service Investigation

Investigated SSH and cron service status using system service-management commands.

**Commands practiced:** `systemctl status ssh`, `systemctl status cron`

*Service names, availability, and `systemctl` support depend on the Linux distribution and environment.*

### Task 11 — Log Investigation

Inspected recent system journal entries and logs associated with the SSH service.

**Commands practiced:** `journalctl -n 20`, `journalctl -u ssh`

### Task 12 — Command Mastery

Practiced the required Linux commands and documented their purposes in a command reference table.

**Commands covered:** Navigation, file operations, permissions, user information, process monitoring, service management, and log investigation.

## 🚀 Bonus — Production Application Scenario

Created a simulated production application directory structure and applied the specified file permissions.

| File | Permission | Purpose |
|---|---|---|
| `configs/prod.env` | `600` | Restricts access to potentially sensitive production configuration |
| `scripts/deploy.sh` | `755` | Allows the deployment script to be executed by users with appropriate access |
| `logs/app.log` | `644` | Allows the owner to write and other users to read the log |

**Key security lessons:**

1. Production environment files must be protected because they may contain credentials and secrets.
2. Deployment scripts need execute permission to run directly as programs, provided their interpreter and other requirements are available.
3. Log files may need to be readable for troubleshooting, but write access should be restricted to appropriate users. Real production logs may require stricter permissions if they contain sensitive information.

**Note:** These permissions are the exercise requirements, not universal production-security recommendations. Actual permissions should follow least privilege and the application's operational requirements.

## 📖 Linux Command Reference

| Command | Purpose |
|---|---|
| `pwd` | Displays the current working directory |
| `ls` | Lists directory contents |
| `ls -la` | Lists all entries, including hidden files, with detailed information |
| `cd` | Changes the current directory |
| `mkdir` | Creates directories |
| `rm` | Removes files or directories, depending on options |
| `touch` | Creates an empty file if it does not exist or updates timestamps |
| `cp` | Copies files or directories |
| `mv` | Moves or renames files and directories |
| `cat` | Displays or concatenates file contents |
| `less` | Views text one screen at a time |
| `nano` | Opens a terminal-based text editor |
| `whoami` | Displays the effective username |
| `id` | Displays user and group IDs |
| `groups` | Displays group memberships |
| `chmod` | Changes file or directory permission bits |
| `sudo` | Runs a command with elevated privileges when authorized |
| `ps aux` | Displays a snapshot of running processes |
| `top` | Provides an interactive process and resource monitor |
| `systemctl` | Manages or inspects systemd services and units |
| `journalctl` | Queries systemd journal logs |

## 📸 Screenshots & Evidence

Screenshots and command outputs should be stored in the repository to demonstrate completion.

Suggested structure:

```text
linux-command-mastery-challenge/
├── README.md
├── screenshots/
│   ├── task-01-directory-structure.png
│   ├── task-02-navigation.png
│   ├── task-03-project-files.png
│   ├── task-04-backups.png
│   ├── task-05-file-organization.png
│   ├── task-06-file-contents.png
│   ├── task-07-permissions.png
│   ├── task-08-user-information.png
│   ├── task-09-process-monitoring.png
│   ├── task-10-service-status.png
│   ├── task-11-system-logs.png
│   └── bonus-production-app.png
├── commands/
│   └── command-reference.md
└── outputs/
    └── command-outputs.txt
```

Only include screenshots, scripts, and outputs that have actually been created. Remove any suggested filenames that you do not use.

## 🔐 Security Considerations

- Never commit real passwords, API keys, access tokens, private keys, or production secrets.
- Use dummy values in practice environment files.
- Review changes before committing them to Git.
- Avoid running destructive commands or commands with elevated privileges without understanding their effects.
- Verify permissions and service status instead of assuming a command succeeded.
- Use least privilege when handling application configuration, deployment scripts, and logs.

## 📚 Key Takeaways

This challenge builds practical familiarity with the Linux command line and establishes a foundation for more advanced work in:

- Linux system administration
- Cloud engineering
- DevOps and CI/CD
- Infrastructure troubleshooting
- Cloud security and DevSecOps

The focus is not just memorizing commands, but understanding what they do, verifying their results, and using them safely.

## 👨‍💻 Author

**Danish John**

BCA Student | Aspiring Cloud Security & DevSecOps Engineer

GitHub: [@danishjohngs](https://github.com/danishjohngs)

---

*This repository is a learning project created for Linux Fundamentals — Week 1 revision and hands-on command-line practice.*
