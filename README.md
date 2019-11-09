# What is this?
Mattermost manifest on the kubernetes.

# How to use

## step1
create Directory on the NFS server which use PV for PostgreSQL.
```bash
root@vagrant:/export/nfs# mkdir mattermost-postgres-pv
root@vagrant:/export/nfs# chmod 777 mattermost-postgres-pv
```

## step2
download manifest and apply them into kubernetes cluster.
```bash
vagrant@vagrant:~$ git clone https://github.com/iguchikoma/mattermost-kubernetes.git
vagrant@vagrant:~$ cd mattermost-kubernetes/
vagrant@vagrant:~/mattermost-kubernetes$ kubectl apply -f mattermost-ns.yaml
vagrant@vagrant:~/mattermost-kubernetes$ kubectl apply -f .
```
