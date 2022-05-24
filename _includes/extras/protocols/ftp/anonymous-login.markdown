{% capture anonymous-login-content %}

FTP clients can be configured to allow users to login using the `anonymous` username. The client may ask for an accompanying password/email but no validation checks are done on it, so in theory you could type in anything.

An anonymous user is usually restricted to the operations they can do; typically they will not have write permissions and therefore cannot upload files (there may be some cases where a separate upload directory has been designated for anonymous users).

An admin may configure a FTP client to allow anonymous logins if they want the hosted files to be accessible by the general public.

An admin can enabled anonymous logins by editing the `vsftp.conf` file on the server machine, which is located at `/etc/vsftp.conf` on the Kali Linux OS.

{% highlight shell %}
# Allow anonymous FTP? (Disabled by default).
anonymous_enable=YES
{% endhighlight %}

{% endcapture %}
{% include extra.html title="FTP Anonymous Login" content=anonymous-login-content %}
