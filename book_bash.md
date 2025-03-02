# Chapter 1: Getting started with Bash 

## Section 1.1: Hello World 

**Interactive Shell**

The bash shell is commonly used **interactively:** It lets you enter and edit commands, then executes them when ypu press the `return` key. Many Unix-based and Unix-like operating systems use Bash as their default shell (notably Linux and macOS). The terminal automatically enters an interactive Bash shell process on startup. 

Output `hello world` typing the following: 

```
echo "Hello World"
#> Hello World #Output Example
```

*Note*

- You can change the shell by just typing the name of the shell in terminal. For example: sh, **bash**, etc. 
- **echo** is Bash builtin command that writes the arguments it receives to the standars output. it ppends a newline to the output, by defult. 

**No-Interactive Shell**

The Bash shell can also be run **non-interactively** from a script, making the shell require no human interaction. Interactive behavior and scripted behavior shoud be identical - and important desing considertation of Unic V7 Bourne shell and transitively Bash. Therefore anything that can be done at the command line can be put in a scipt file for reuse. 

Follow these steps to create a Hello world script: 

1. Create a new file called hello-world.sh 

    terminal\
    `touch hello-world.sh`

2. Make the script executable by runnung `chmod +x hello-world.sh`
3. Add this code:

    ```
    #!/bin/bash
    echo "hello World" 
    ```
    **Line 1**: The first line of the script must start with the character sequence `#!`, referred to as *shebang1*. The shebang instructs the operating system to run `/bin/bash`, the Bash shell, passing it the script's path as an argument. 

    E.g. `/bin/bash hello-world.sh`

    **Line 2**: Uses the `echo`command to write `Hello World`to the standard output. 

4.  Execute the `hello-world.sh`script from the command line using one of the following: 
       - `./hello-world.sh` - most commonly used, adn recommended 
       - `/bin/bash hello-world.sh`.
       - `bash hello-world.sh`- assuming `/bin`is in your `$PATH`
       - `sh hello-word.sh`
  
For real production use, you would omit the `.sh` extension  (which is misleading anyway, since this is a Bash script, not a `sh` script) and perhaps move the file to a directory within your __PATH__ so that it is available to you regardless of your current workging directory, just lika a system command such as `cat` or `ls`