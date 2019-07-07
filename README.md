```
关于nfs用于搭建本地仓库做离线的主包及其依赖
# yum -y install yum-utils
# yum -y install createrepo

# repotrack nfs-utils rpcbind -p /root/nfsDeps
# createrepo -v /root/nfsDeps
# cd /root/nfsDeps
# tar -zcf  nfs.tar.gz  ./*

# cp nfs.tar.gz role/yumRepo/files
```
