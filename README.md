# juypter-launcher
Launch jupyter-lab on docker.

### Overview
You can run juypter-lab container in any directory and handle files on local.  


### Require
- docker

If you want to run jupyter with gpu, you need to prepare gpu environment. Please check [setup_ec2](https://github.com/kenchalros/setup_ec2).

### How to use
1. **Get scripts in your worknig directory.**  
    You can get a `launch` sciprt and `dockerfiles` directory to execute the following commands.
    ```
    wget --no-check-certificate https://github.com/kenchalros/jupyter-launcher/archive/master.tar.gz
    tar -xvzf master.tar.gz
    rm jupyter-launcher-master/README.md
    mv jupyter-launcher-master/* .
    rm -r jupyter-launcher-master/
    rm master.tar.gz
    ```
1. **Execute `launch`**  
Execute `./launch cpu` or `./launch gpu` ( `gpu` needs another setting. ).  
`launch` command requires one param `cpu` or `gpu`. Option `-h` gives more infomation.

1. **Access port `8888` in browser.**  
If you execute `launch` command on local machine, you can access `localhost:8888` .
In the case of execute on remote server, you can access `<hostname>:8888`


### How to custom
This repo has 2 dockerfiles. If you need to custom jupyter-lab, please edit dockerfile.  
( `dockerfile_cpu` is executed `launch cpu` command, and `dockerfile_gpu` is executed `launch gpu`. )
