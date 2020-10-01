# juypter-launcher
Launch jupyter-lab on docker.

### Overview
You can run juypter-lab container in any directory and handle files on local.  


### Require
- docker

If you want to run jupyter with gpu, you need to prepare gpu environment. Please check [setup_ec2](https://github.com/kenchalros/setup_ec2).

### How to use
1. **Clone this repository.**
    ```
    git clone https://github.com/kenchalros/jupyter-lauhcher.git
    ```
1. **Execute `launch`**
Execute `launch cpu` or `launch gpu` ( `gpu` needs another setting. ) in the directory that you want to run jupyter-lab ( recommended to register an alias or add path to execute `lauhch`. ) .  
`launch` command requires one param `cpu` or `gpu`. Option `-h` gives more infomation.

1. **Access port `8888` in browser.**
If you execute `launch` command on local machine, you may access `localhost:8888` .
In the case of execute on remote server, you may access `<hostname>:8888`


### How to custom
This repo has 2 dockerfiles. If you need to custom jupyter-lab or docker image, please edit dockerfile.  
( `dockerfile_cpu` is executed `launch cpu` command, and `dockerfile_gpu` is executed `launch gpu`. )
