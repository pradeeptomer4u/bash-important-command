# bash-important-command
bash important command


  # Bash Changes Start #
    virtualenv_info (){
        # Get Virtual Env
        if [[ -n "$VIRTUAL_ENV" ]]; then
            # Strip out the path and just leave the env name
            venv="${VIRTUAL_ENV##*/}"
        else
            # In case you don't have one activated
            venv='Default | Environment'
        fi
        [[ -n "$venv" ]] && echo "$venv"
    }
  # VENV Wrapper
    export WORKON_HOME=$HOME/.virtualenvs
    export PROJECT_HOME=$HOME/
    export VIRTUALENVWRAPPER_PYTHON='/usr/bin/python3'
    source /usr/local/bin/virtualenvwrapper.sh
    alias mkproject='mkproject --python=/usr/local/bin/python3.7'
# Exports
    export EDITOR=vim

# Python Related Alias
    alias py='python3'
# alias python='python2'
    alias pip='pip3'
    alias bpython='bpython3'

# Git Alias
    alias gi='git init'
    alias gc='git commit'
    alias gp='git push'
    alias gf='git fetch && git rebase'
    alias gr='git rebase'
    alias gs='git status'
    alias gl='git lg'
    alias gd='git diff'

# Linux Alias
    alias bye='sudo shutdown -h now'
    alias install='sudo apt -y install'
    alias remove='sudo apt -y remove'
    alias update='sudo apt -y update'
    alias upgrade='sudo apt -y update && sudo apt -y upgrade'
    alias clean='sudo apt-get autoclean && sudo apt-get autoremove'
    alias ..='cd ..'
    alias ...='cd ../..'
    alias ....='cd ../../..'
    alias .....='cd ../../../..'

# Empty the trash folder that is created when you delete things as root
    alias root_trash='sudo bash -c "exec rm -r /root/.local/share/Trash/{files,info}/*"'

# Django Alias
    alias csu='python3 manage.py createsuperuser'
    alias run='python3 manage.py runserver 8888'
    alias mm='python3 manage.py makemigrations'
    alias migrate='python3 manage.py migrate'
    alias shell='python3 manage.py shell'

# Other Alias
    alias top='top -o cpu'
    alias ..='cd ..'
    alias dev='cd ~/Documents/'
    alias l='ls -CF'

