# 简介
> 这个工程主要是运用Ansible解决运维自动化部署问题.Ansible安装可以自行科普.

# 项目结构
```
.
├── README.md
├── deploy
│   ├── deploy_roles.yml
│   ├── files -> /Users/lixin/WorkspaceAnsible/files              # 指向的是软链接
│   ├── handlers
│   │   └── main.yml
│   ├── tasks
│   │   ├── def-vars.yml
│   │   ├── deploy.yml
│   │   ├── init.yml
│   │   ├── main.yml
│   │   └── service.yml
│   ├── templates
│   │   └── app.sh.j2
│   └── vars
│       └── main.yml
├── jdk
│   ├── files
│   │   └── jdk-8u271-linux-x64.tar.gz
│   ├── handlers
│   ├── jdk_roles.yml
│   ├── tasks
│   │   ├── config-env-var.yml
│   │   ├── install.yml
│   │   ├── main.yml
│   │   └── ready-install.yml
│   ├── templates
│   │   └── jdk.sh.j2
│   └── vars
│       └── main.yml
└── mysql
    ├── files
    │   ├── mysql-5.7.34-linux-glibc2.12-x86_64.tar.gz  
    │   └── mysqld                                        # 从tar.gz提取出来
    ├── handlers
    │   └── main.yml
    ├── mysql_roles.yml
    ├── tasks
    │   ├── add-user-and-group.yml
    │   ├── config-limits-conf.yml
    │   ├── install.yml
    │   └── main.yml
    ├── templates
    │   ├── my.cnf.j2
    │   └── rc.local.j2
    └── vars
        └── main.yml



# 这个目录可以是运维定义的一个发版目录(建议扔到git仓库上或者通过sync).
lixin-macbook:ansible_roles lixin$ tree /Users/lixin/Desktop/ansible_files/
/Users/lixin/Desktop/ansible_files/
└── test-service
    └── 2019-09-20
        └── 18.20
            ├── conf
            │   └── application.properties
            └── lib
                └── hello-service.jar

```
# 注意事项
> 在上传到git时,我这边是去除了*.tar.gz   

# 参考文章
["自动化运维解决方案"](https://www.lixin.help/2019/09/20/Ansible-AutoDeploy.html)
