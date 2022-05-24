{% capture no-root-squash-content %}
`no_root_squash` is an option that can be set when configuring the `/etc/exports` file to setup a NFS share.

If set, it allows a root user who connects to the NFS share to keep the same privileges that a local superuser would have.

{% endcapture %}

{% include extra.html title="no_root_squash" content=no-root-squash-content %}
