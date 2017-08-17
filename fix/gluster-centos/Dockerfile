FROM gluster/gluster-centos:latest

RUN mv /usr/bin/systemctl /usr/bin/systemctl_real
ADD systemctl /usr/bin/
RUN chmod 775 /usr/bin/systemctl
ENV SYSTEMD_IGNORE_CHROOT 1
CMD ["/usr/lib/systemd/systemd","--system"]
