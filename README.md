bosh-zsh-autocompletion
=======================

Oh My Zsh (or probably any zsh but YMMV) plugin for BOSH autocompletion. 

See the know issues below for what doesn't work.

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
    ➜  ~  bosh ......                                                                  
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
    
    ➜  ~  bosh de<tab>                                                            
    delete                 deployment             destination_directory
    deploy                 deployments

    ➜  ~  bosh delete <tab>
    deployment  release     snapshot    snapshots   stemcell    user
    
    ➜  ~  bosh delete s<tab>
	snapshot   snapshots  stemcell
	
#Known Issues
It's crazy slow with the AWS plugin installed. This is a BOSH thing, on my laptop it takes ~9s to output the help. Thankfully we cache it once per terminal session. If you were to upgrade the gem and the usage changed this will cause a problem. Restart your shell and you'll be good to go. 

```destination_directory``` shows up when it shouldn't because of the way the CLI for ```run_errand``` wraps the help for the command. Not sure if this is a bug in the CLI or if I should workaround it. 

    run errand [<errand_name>] [--download-logs] [--logs-dir
    destination_directory] [--keep-alive]``

#Problems? 
Open an issue or submit a PR please!
