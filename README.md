# docker-env
Interactively manage different docker connection environments on your terminal

## Installation
* copy the `docker` script to your local `$PATH` (e.g. `~/bin/`)
* make it executable with `chmod +x ~/bin/docker`
* maybe you have to adjust the path of your docker binary by editing the `docker="…"` variable in the script
* add you docker environments by defining new function similar to predefined examples (`dockerenv_local ()` and `dockerenv_remote1 ()`)
* to have the interactive environment selection in place add the following line to your `~/.profiles`, `~/.bashrc`, `~/.zshrc` or which ever is used for your shell


    export DOCKER_ENV="local"   # set the default environment to local
    alias docker-env="eval \$(docker select-env)"

## Usage

    $ docker-env        # select the current docker environment
    $ docker list-env   # list all available environments and show the active env
    $ docker …          # just use all the other docker commands as usual, they are redirected to your docker binary
