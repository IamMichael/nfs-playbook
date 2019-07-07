```
基于CentOS7.5 Minimal 安装测试
关于nfs用于搭建本地仓库做离线的主包及其依赖
# yum -y install yum-utils
# yum -y install createrepo

# repotrack nfs-utils rpcbind -p /root/nfsDeps
# createrepo -v /root/nfsDeps
# cd /root/nfsDeps
# tar -zcf  nfs.tar.gz  ./*

# cp nfs.tar.gz role/yumRepo/files


安装nfsServer和nfsClient
# ansible-playbook -i hosts  install_nfs.yml

卸载nfsClient、nfsClient 和 本地仓库
# ansible-playbook -i hosts un_nfsClient.yml
# ansible-playbook -i hosts un_nfsServer.yml
# ansible-playbook -i hosts un_yumRepo.yml


```
