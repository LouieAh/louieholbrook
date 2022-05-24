{% capture http-server-content %}
The `http.server` python module can be used to create a server which serves files relative to the current directory the module is run from.

The server listens by default on port `8000`, although this can be overridden by passing the desired port number as an argument:

{% highlight shell %}
# Serve on port 9000
$ python -m http.server 9000
{% endhighlight %}

Requests for files can then be made from another machine to the machine hosting the python server. For instance, say the `http.server` module is run on a machine with IP `10.11.68.55`, using the default port `8000`, in order to share the file `share.txt`. Another machine can make a GET request to retrieve this file to their machine.

{% highlight shell %}
$ wget http://10.11.68.55:8000/share.txt
{% endhighlight %}

{% endcapture %}

{% include extra.html title="Python http.server"  content=http-server-content %}
