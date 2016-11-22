# Terminal

### Setting
```
$ nano .bash_profile 
```  
* ctrl+O to save  
* ctrl+X to Exit  

**my .bash_profile**
```
export PS1="\[\e[32;1m\]\W \[\e[36;1m\]\u$ \[\e[0m\]"
export CLICOLOR=1
export LSCOLORS=DxFxBxDxdxegedabagacad
alias ls='ls -GFh'
```  
* PS1 : path and username setting

### Commands
* open . : open finder in current path

### References
[**IBM** Tip: Prompt magic](http://www.ibm.com/developerworks/linux/library/l-tip-prompt/)  
[Add Color to the Terminal in Mac OS X](http://osxdaily.com/2012/02/21/add-color-to-the-terminal-in-mac-os-x/)