# code
```sh
parse_git_fg() {
  if [[ $(git status -s 2> /dev/null) ]]; then
    echo -e "\033[0;31m"
  else
    echo -e "\033[0;32m"
  fi
}

PS1='\[\e[0;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[$(parse_git_fg)\]$(__git_ps1)\[\033[0;32m\]\[\033[0m\]\$ '
```

# setup
 add to ~/.bashrc file this code on the end