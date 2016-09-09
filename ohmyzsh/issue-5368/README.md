Docker image to reproduce the segfault error reported at
https://github.com/robbyrussell/oh-my-zsh/issues/5368.

## Features

- System: Ubuntu 14.04

- Zsh: 5.0.2

- Taskwarrior: 2.5.1 (compiled from source)

Also includes `gdb`.

## How to reproduce

1. Run image with:
   `docker run -it mcornella/ohmyzsh-5368`

2. Run a subshell so as to avoid crashing the docker container:
   `zsh`

3. Type `task `, then press TAB. The following should appear:
   `zsh: segmentation fault (core dumped)  zsh`
