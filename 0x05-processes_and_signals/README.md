# 0x05. Processes and Signals

## Overview

In this project, we explore the concepts of processes and signals in the world of Unix-based operating systems. Understanding how processes work and how to manage them using signals is crucial for building robust and efficient software systems.

## Learning Objectives

By the end of this project, you will have a solid understanding of the following concepts:

- **Processes:** Learn what processes are, how they are created, and how they interact with the operating system.

- **Signals:** Understand how signals work, how to send and receive signals in a Unix environment, and how to handle them in your programs.

- **Process Management:** Explore techniques for managing processes, including creating child processes, monitoring their status, and terminating them gracefully.

## Project Files

This project includes the following files and directories:

- `0-what-is-my-pid`: A Bash script that prints the current process ID (PID) of the script itself.

- `1-list_your_processes`: A Bash script that displays all running processes. It filters out the `grep` command used for filtering.

- `2-show_your_bash_pid`: A Bash script that displays the PID of the parent shell (Bash) and the script itself.

- `3-show_your_bash_pid_made_easy`: A Bash script that displays the PID of the parent shell (Bash) without using `grep`.

- `4-to_infinity_and_beyond`: A Bash script that launches an infinite loop and sends the `SIGTERM` signal to itself.

- `5-kill_me_now`: A Bash script that kills the `4-to_infinity_and_beyond` script.

- `6-kill_me_now_made_easy`: A Bash script that kills the `4-to_infinity_and_beyond` script without using its PID.

- `7-highlander`: A Bash script that displays "To be or not to be" indefinitely, ignoring the `SIGTERM` signal.

- `8-beheaded_process`: A Bash script that kills the `7-highlander` script.

- `100-process_and_pid_file`: A Bash script that creates a file containing the PID of a given process and deletes it when the process is terminated.

- `101-manage_my_process`: A Bash script that manages the `manage_my_process` Python script by sending specific signals.

- `manage_my_process`: A Python script used in conjunction with `101-manage_my_process` to demonstrate process management with signals.

## Getting Started

You can execute the Bash scripts by running them in a Unix-like terminal environment. Make sure the scripts have the appropriate execute permissions using the `chmod` command:

```bash
chmod +x <script_name>
```

To run the scripts:

```bash
./<script_name>
```

For the Python script (`manage_my_process`), you can run it as follows:

```bash
python manage_my_process
```

## Usage

Feel free to explore the code and experiment with different signals and processes. Understanding processes and signals is crucial for developing robust and responsive applications in a Unix environment.

