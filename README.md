bosh-zsh-autocompletion
=======================

Oh My Zsh plugin for BOSH autocompletion

Installation 
============

Drop the ```bosh``` directory into your ```$ZSH/custom/plugins/``` (usually ```~/.oh-my-zsh/custom/plugins```) directory. Then add bosh to the plugins line of your ```.zshrc``` file. For example here's my ```.zshrc``` plugin lines

    # Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
    # Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
    # Example format: plugins=(rails git textmate ruby lighthouse)
    # Add wisely, as too many plugins slow down shell startup.
    plugins=(git docker jsontools tmux vagrant bosh)
    
    
#Example

Type ```bosh <tab>``` and watch the magic happen

    Last login: Thu Dec 11 16:42:19 on ttys002
    ➜  ~  bosh ......                                                                  $
    add                    generate               ssh
    alias                  get                    start
    aliases                help                   status
    backup                 import                 stemcells
    blobs                  init                   stop
    cancel                 locks                  sync
    cleanup                login                  take
    cloudcheck             logout                 target
    complete               logs                   targets
    create                 properties             task
    delete                 public                 tasks
    deploy                 recreate               unset
    deployment             releases               upload
    deployments            rename                 validate
    destination_directory  reset                  verify
    diff                   restart                version
    download               run                    vm
    edit                   scp                    vms
    errands                set
    export                 snapshots
    
