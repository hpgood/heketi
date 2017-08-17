
in docker 17.06, run systemctl status glusterd ,it will throw a error sometimes:


please build a custom image ,using:
  https://github.com/hpgood/heketi/blob/master/fix/gluster-centos/Dockerfile and
  https://github.com/hpgood/heketi/blob/master/fix/gluster-centos/systemctl

docker build -t gluster/gluster-centos:custom  .

Please edit glusterfs-daemonset.yaml,and change 
  gluster/gluster-centos:latest
to:
  gluster/gluster-centos:custom
  
