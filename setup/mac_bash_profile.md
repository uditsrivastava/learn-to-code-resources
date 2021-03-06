# Create a Bash Profile on Mac

**STEP 1**

Launch Terminal and make sure you are in your home directory by entering `pwd`:

```bash
pwd
```
If your mac user name is **dan**, the output should read:

```
/Users/dan
```

**STEP 2**

If you don't already have a .bash_profile, you can create one with the `touch` command:

```bash
touch .bash_profile
```

**STEP 3**  

Confirm that the file is there by entering `ls -a`. Because your **.bash_profile** is a dotfile, it will not be visible without the `-a` option.

**STEP 4**  

Open your **.bash_profile** in Atom by entering `atom .bash_profile`.

**STEP 5**

Here's a script that will get you going with custom colors for your `ls` output.

```bash
export LSCOLORS=CxGxFxdxCxDxDxaccxaeex

alias ls='ls -Gh'
```

Save your **.bash_profile**, then from the command line, enter `source .bash_profile`.

Enter `ls` to see your directory contents output in color.  

See [this osxdaily article](http://osxdaily.com/2012/02/21/add-color-to-the-terminal-in-mac-os-x/) to do even more with your LSCOLORS!

**STEP 6 (Optional)**

To customize your prompt, you can use the `PS1` environment variable. Here's a simple, custom prompt to get you going! Write this script anywhere in your *.bash_profile*.

```bash
export PS1="\d \t \u \w $ "
```

* `\d` will display the date
* `\t` will display the time
* `\u` will display the user name of the current user
* `\w` displays the working directory

Don't forget to enter `source .bash_profile` after you save your script. You also may need to launch a new Terminal session to register the change. 

[Learn more about the `PS1` variable here!](http://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
