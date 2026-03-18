开源软件开发学习

付喆


总结：
********
git remote add origin git@github.com:OSSD-Course-SYSU-2/2026spring-25307036-lab1.git


git add .
git add 文件1 文件2 文件3
git add 文件夹名/                                  #添加某个文件夹里的文件
git add *.py                                          #添加某种类型的文件

git commit -m'***'
git push origin dev

git rm 文件名

git clone git@***.git 文件夹名
cd 文件夹
git branch dev
git checkout dev   ###选择分支dev 也可以换成别的 如master
git branch            ###查看分支

wsl设置密钥：{
ls -al ~/.ssh                                                    #查看现成的ssh密钥
ssh-keygen -t ed25519 -C "你的GitHub邮箱"   #一把私钥，留在你电脑里   一把公钥，上传到 GitHub  随后会设置地址和密码
eval "$(ssh-agent -s)"                                     #启动 ssh-agent。它是一个帮你暂时保管已解锁私钥的进程。
ssh-add ~/.ssh/id_ed25519                            #私钥id_ed25519  加入ssh-agent    成功：Identity added: ...
ssh-add -l                                                      #检查agent有没有加载成功 列出已经加载的密钥
cat ~/.ssh/id_ed25519.pub                             #查看公钥内容

在github里添加公钥

ssh -T git@github.com                                  #测试ssh是否连接上github

ssh-keygen -p -f ~/.ssh/id_ed25519               #重新设置密码
ssh-add ~/.ssh/id_ed25519                            #重新加载key 把私钥重新加入agent