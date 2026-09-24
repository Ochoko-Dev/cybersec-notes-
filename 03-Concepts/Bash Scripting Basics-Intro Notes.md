# Bash Scripting Basics — Intro Notes

## echo
`echo` makes the terminal print back whatever text follows it.

```bash
echo "hi mom"
```
Output: `hi mom`

## Automating output with a script
To automate this instead of typing commands one at a time, we write a script using the **nano** text editor.

```bash
nano himom.sh
```

This opens (or creates) `himom.sh` for editing. The `.sh` extension just signals it's a shell script.

Inside the editor, the first line is the **shebang**:

```bash
#!/bin/bash
```

`#!` tells the terminal which scripting language to run the file with — here, bash. Then we write:

```bash
echo "hi mom"
```

That's the first script — save and exit.

## Running the script
```bash
bash himom.sh
```

This runs the script and prints `hi mom`.

## Adding more to the script
Reopen the file with nano and add more commands. We can also use `sleep` to pause between outputs:

```bash
echo "hi mom"
sleep 3
echo "uh huh"
```

This prints `hi mom` immediately, waits 3 seconds, then prints `uh huh`.

## Permissions: running with ./
Trying to run the script directly:

```bash
./himom.sh
```

...gives a **Permission denied** error, because the file only has read/write permissions, not execute.

Fix with `chmod` (changes file permissions):

```bash
chmod +x himom.sh
```

`+x` adds the executable permission. Now:

```bash
./himom.sh
```

...runs successfully.

## Variables
Say `bestdayever.sh` has several lines repeating a name, e.g. "choxii":

```
Good morning choxii
You are looking good today choxii
You have the best beard i have ever seen choxii
```

Instead of manually editing "choxii" everywhere, we introduce a **variable**:

```bash
name="slatt"
```

Then replace every "choxii" with `$name`. Now all lines automatically use "slatt" instead.

## Making it interactive with read
We're still hardcoding the name manually. To let the script ask for it instead:

```bash
echo "what is your name?"
read name
```

Now every time the script runs, it prompts for a name and substitutes it everywhere `$name` appears.

## Positional parameters
Instead of prompting interactively, we can pass the name as an **argument** when running the script — a positional parameter:

```bash
name=$1
```

Running:
```bash
./bestdayever.sh lene
```
Output:
```
Good morning lene
You are looking good today lene
You have the best beard i have ever seen lene
```

We can add a second positional parameter too:

```bash
compliment=$2
```

Replace "beard" with `$compliment`. Running:
```bash
./bestdayever.sh leo eyes
```
Output:
```
Good morning leo
You are looking good today leo
you have the best eyes i have ever seen leo
```

## Useful built-in commands
- `whoami` — shows the currently logged-in user
- `pwd` — shows the current working directory
- `date` — shows today's date

## Storing command output in variables
We can capture the output of these commands using command substitution:

```bash
user=$(whoami)
date=$(date)
whereami=$(pwd)
```

Then use them in output:

```bash
echo "you are currently logged in as $user and you are in the directory $whereami. Also today is: $date"
```

Running `./bestdayever.sh leo eyes` now outputs:
```
Good morning leo
You are looking good today leo
You have the best eyes i have ever seen leo
you are currently logged in as leone and you are in the directory /home/leone. Also today is: Tue Sep 22 03:55:15 AM EDT 2026
```

---

# Day 2

## Combining read prompts
Script `getrichquick.sh`:

```bash
#!/bin/bash
echo "what is your name?"
read name
echo "how old are you?"
read age
echo "hello $name, you are $age years old"
```

Prompts for name, then age, then prints a greeting combining both — e.g. "hello leone, you are 21 years old".

## $RANDOM
`$RANDOM` is a built-in variable that generates a random number between 0 and 32767 each time it's referenced.

## Custom variables and export
```bash
twitter="elon musk"
echo $twitter
```
Prints "elon musk" — but as-is, this variable can't be used by child processes.

To make it available to child processes, convert it into an **environment variable**:

```bash
export twitter
```

However, this doesn't persist — closing the terminal and reopening it, `echo $twitter` prints nothing, because the variable was never made permanent.

## Making variables permanent
Quick tip: in Linux, a file starting with `.` (dot) is hidden.

To persist the variable, edit `.bashrc`:

```bash
nano .bashrc
```

Add:
```bash
export twitter="Elon Musk"
```

Now the variable survives logging out and back in.

## Arithmetic expressions
```bash
echo $(( 2+5 ))
```
Prints `7`. Subtraction, multiplication, and division work the same way — but bash arithmetic doesn't support floating-point numbers.

Using `$RANDOM` with modulo to get a bounded range:

```bash
echo $(( $RANDOM % 10 ))
```
Generates a random number between 0–9 each time (modulo 10 caps the range).

## Putting it together: getrichquick.sh
Add a new variable combining `$RANDOM`, modulo, and the earlier `$age` variable:

```bash
getrich=$(( ($RANDOM % 15) + $age ))
echo "$name, you will become a millionaire when you are $getrich years old"
```