# Dotfiles
my very convinient dotfiles everybody should start using right away



# Useful .bashrc Utils

You should add the following pieces of code to your `~/.bashrc` immediately

## Custom Prompt for None Zero Return

Add this to never let a command silently fail

```.bash
function nonzero_return() {
        RETVAL=$?
        if [ $RETVAL -ne 0 ];
        then
                echo -e " \e[41m!!!\e[m "
        else
                echo " "
        fi
}

export PS1="\[\e[32m\]\[\e[1m\]\h\[\e[m\]:\[\e[34m\]\[\e[1m\]\\w\[\e[m\]\\$\`nonzero_return\`"

```


