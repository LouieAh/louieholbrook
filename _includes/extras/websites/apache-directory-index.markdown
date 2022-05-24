{% capture directory-index-content %}
For websites hosted on a server that is running Apache, a directory index can be configured to be returned by setting the `Options +Indexes` option for the particular directory. This is done within the Apache `.conf` (configuration) file, which is by default located at `usr/local/apache2/conf/httpd.conf`. <a href="https://cwiki.apache.org/confluence/display/HTTPD/DirectoryListings" target="_blank">Read more here</a>.

{% highlight shell %}
# /usr/local/apache2/httpd.conf
...
<Directory /var/www/html/backups>
  Options +Indexes
</Directory>
...
{% endhighlight%}
{% endcapture %}

{% include extra.html title="Apache Directory Indexes" content=directory-index-content %}
