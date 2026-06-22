# ZSECURITY Terminal Banner Setup (Kali Linux)

Create a custom hacker-style terminal banner in Kali Linux using Figlet, Lolcat, and Zsh.

## Prerequisites

Update your system and install the required packages:

```bash
sudo apt update
sudo apt install figlet lolcat -y
```

Verify installation:

```bash
figlet ZSECURITY | lolcat
```

---

## Check Your Shell

Determine which shell you are using:

```bash
echo $SHELL
```

Example output:

```bash
/bin/zsh
```

Kali Linux uses **Zsh** by default, so the configuration must be added to `.zshrc`.

---

## Configure the Startup Banner

Open the Zsh configuration file:

```bash
nano ~/.zshrc
```

Scroll to the bottom and add:

```bash
clear
figlet ZSECURITY | lolcat
```

For a more stylish banner:

```bash
clear
figlet -f cyberlarge ZSECURITY | lolcat
```

---

## Save the File

Inside Nano:

* Press `Ctrl + O`
* Press `Enter`
* Press `Ctrl + X`

---

## Apply Changes

Reload the configuration:

```bash
source ~/.zshrc
```

Or close and reopen the terminal.

---

## Verify Configuration

Check the last lines of `.zshrc`:

```bash
tail -5 ~/.zshrc
```

Expected output:

```bash
clear
figlet ZSECURITY | lolcat
```

---

## Troubleshooting

### Banner does not appear

Check your shell:

```bash
echo $SHELL
```

If the output is:

```bash
/bin/zsh
```

Use:

```bash
~/.zshrc
```

not:

```bash
~/.bashrc
```

### Figlet command not found

Install Figlet:

```bash
sudo apt install figlet -y
```

### Lolcat command not found

Install Lolcat:

```bash
sudo apt install lolcat -y
```

---

## Example Output

```text
███████╗███████╗███████╗ ██████╗██╗   ██╗██████╗ ██╗████████╗██╗   ██╗
╚══███╔╝██╔════╝██╔════╝██╔════╝██║   ██║██╔══██╗██║╚══██╔══╝╚██╗ ██╔╝
  ███╔╝ ███████╗█████╗  ██║     ██║   ██║██████╔╝██║   ██║    ╚████╔╝
 ███╔╝  ╚════██║██╔══╝  ██║     ██║   ██║██╔══██╗██║   ██║     ╚██╔╝
███████╗███████║███████╗╚██████╗╚██████╔╝██║  ██║██║   ██║      ██║
╚══════╝╚══════╝╚══════╝ ╚═════╝ ╚═════╝ ╚═╝  ╚═╝╚═╝   ╚═╝      ╚═╝
```

## Author

**ZSECURITY**

Custom Kali Linux terminal banner using Zsh, Figlet, and Lolcat.
