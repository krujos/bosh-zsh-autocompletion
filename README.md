bosh-zsh-autocompletion
=======================

Oh My Zsh plugin for BOSH autocompletion

Installation 
============

Drop the ```bosh``` directory into your ```$ZSH/custom/plugins/``` (usually ```~/.oh-my-zsh/custom/plugins```) directory. Then add bosh to the plugins line of your ```.zshrc``` file. For example here's my ```.zshrc``` plugins lines

    # Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
    # Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
    # Example format: plugins=(rails git textmate ruby lighthouse)
    # Add wisely, as too many plugins slow down shell startup.
    plugins=(git docker jsontools tmux vagrant bosh)