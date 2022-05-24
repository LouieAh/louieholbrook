{% capture etc-exports-content %}
Part of the process of sharing a directory with NFS involves editing the `/etc/exports` file on the server machine.

As explained {% include link.html href="https://web.mit.edu/rhel-doc/5/RHEL-5-manual/Deployment_Guide-en-US/s1-nfs-server-config-exports.html" text="here" end="," %} each line within this file relates to an exported directory, with the following structure:
{% highlight plaintext %}
<export> <host1>(<options>) <hostN>(<options>)
{% endhighlight %}

So, for `/home/public *(rw,sync,no_root_squash,insecure)`:

| Syntax | General meaning |
| --- | --- |
| `/home/public` | The directory to be shared |
| `*` | Share with anyone who can connect |
| `(rw,sync,no_root_squash,insecure)` | The NFS options for the shared directory |

{% include link.html href="https://www.golinuxcloud.com/unix-linux-nfs-mount-options-example/" text="This article" %} explains NFS options really well.

{% endcapture %}

{% include extra.html title="/etc/exports" content=etc-exports-content %}
