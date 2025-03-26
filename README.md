# 🚀 Automation Testing of Linux Commands Using Git-hub Actions

This project demonstrates how Linux sysadmin tasks can be automated and tested in a CI/CD environment (like GitHub Actions) — which is a real-world DevOps/Automation scenario.

Each Linux command category is stored in a separate folder with a corresponding `.txt` file. These commands are executed automatically when changes are pushed to the repository or manually triggered via GitHub Actions.



## 🏗️ Project Structure

```
Automation-testing-of-linux-command/
├── linux_basic_commands/
|   └── linux_basic_commands.txt
├── logs_management/
│   └── logs_commands.txt
├── memory_disk_management/
│   └── memory_disk_commands.txt 
├── network_management/
│   └── network_commands.txt
├── package_management/
|   └── package_management_commands.txt
├── process_management/
│   └── process_commands.txt
├── user_access_management/
│   └── user_access_commands.txt 
└── .github/
    └── workflows
        ├── log_analysis.yml
        ├── network_diagnositcs.yml
        ├── package_management_workflow.yml
        ├── process_management_workflow.yml
        ├── system_resource_check.yml
        ├── test_shell_commands.yml
        └── user_group_management_workflow.yml

```
## ⚙️ How It Works
```

When a `.txt` file is pushed or manually triggered, GitHub Actions will:
  1. Read all lines from the file.
  2. Skip blank lines or lines starting with `#` (comments).
  3. Execute each command one by one.
  4. Display command outputs and errors.
  5. Show a success/failure message after each command.

```
## 🚦 Workflow Triggers
```
------------------------------------------------------------------------
| Trigger Type        | Description                                    |
|---------------------|------------------------------------------------|
| `push`              | When `.txt` command files are pushed or changed|
| `workflow_dispatch` | Manual trigger from GitHub UI                  |
------------------------------------------------------------------------


```
## 📜 Commands Categories
```
----------------------------------------------------------------------------------------
|    Category	        | Description                                                  |
|--------------------------------------------------------------------------------------|
|⚙️ Basic Commands	| Disk usage, file permissions, service status, directories    |
|👨‍🦱 User Management    | Create users, modify groups, manage sudoers, change passwords|                                                            |
|📂 Logs Management	| Analyze logs, view dmesg, journalctl, boot logs              |
|💾 Memory Management	| Check memory/swap usage, buffers, cache, top/htop            |
|🌐 Network Management	| Check IPs, ping, DNS, traceroute, netstat, ss                |
|📦 Package Management	| Install, remove, update software packages                    |  
|🔄 Process Management	| Manage processes, kill, background jobs, resource usage      |
----------------------------------------------------------------------------------------
```

``
## ✅ Real-World Use Cases
```
🔍 Validate your Linux skills in a DevOps CI pipeline.
🔄 Build automation-ready Linux command modules.
📚 Prepare for Linux/DevOps job interviews.
👨‍💻 Practice shell scripting in a controlled environment.
📊 Showcase it in your resume/GitHub portfolio.

```
## 🏁 Getting Started
```
✅ Fork or Clone the repository.
📝 Add or modify commands in the relevant .txt file.
🔀 Push changes to trigger the workflow automatically.
⚙️ Or, go to GitHub Actions and click “Run Workflow” manually.
📊 Check the execution results under the Actions tab.

```
## ✍️ Author
```
Akhil Thyadi
GitHub: [@akhil27051999](https://github.com/akhil27051999)

```
## 📜 License
```
This project is open source and available under the [MIT License](LICENSE).

