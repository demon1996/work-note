# git ssh公钥配置
## 生成公钥
    查看用户目录下有没有.ssh文件夹，如果有，查看是否有id_rsa和id_rsa.pub文件，如果有跳过这一步
    如果没有打开shell 创建ssh key
    
    ssh-keygen -t rsa -C "youremail@example.com"
    
    一路回车，使用默认即可，也可以选择设置密码
    
    一切顺利的话会在用户目录下生成.ssh目录，里边有id_rsa和id_rsa.pub两个文件，id_rsa是私钥，不能泄漏，id_rsa.pub是公钥
## 添加公钥
    以github为例
    cat ～/.ssh/id_rsa.pub 查看公钥复制
    登录github－>settings->SSH and GPG keys
    点击Add SSH Key 填写任意title 在key文本框里粘贴id_rsa.pub文件的内容
    点击Add Key 验证通过后即可