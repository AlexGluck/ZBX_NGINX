<h2>System requirements</h2>
<p><a title="Nginx" href="http://nginx.org/" target="_blank">Nginx</a>, with configured `http_stub_status_module`</p>
<h2>Features</h2>
<h5>HTTP/HTTPS support</h5>
<h5>Connection Statistics:</h5>
<ul>
<li>Active</li>
<li>Reading</li>
<li>Waiting</li>
<li>Writing</li>
</ul>
<h5>Request Statistics:</h5>
<ul>
<li>Accepted</li>
<li>Handled</li>
<li>Total</li>
</ul>
<h5>Graph and screen:</h5>
<ul>
<li>'Requests Statistics' graph</li>
<li>'Connection Status' graph</li>
<li>Screen combining both graph</li>
</ul>
<h5>Macros for customization:</h5>
<ul>
<li>{$NGINX_HOST}</li>
<li>{$NGINX_STATS_URI}</li>
<li>{$NGINX_PORT}</li>
<li>{$NGINX_REQ_NUM}</li>
<li>{$NGINX_CON_NUM}</li>
</ul>
<h2>Installation</h2>
<h3>Nginx Configuration</h3>
<p> </p>
<p>Add the following example to your default vhost configuration file:</p>
<pre>location /nginx_status {<br />    stub_status on;<br />    access_log off;<br />    allow 127.0.0.1;<br />    allow ::1;<br />    deny all;<br />}</pre>
<pre> </pre>
<h3>Zabbix Configuration</h3>
<p> </p>
<ol>
<li>Import XML template file (`zbx_template_nginx.xml`) into Zabbix via Web GUI (Configuration -&gt; Templates -&gt; Import).</li>
<li>Assign the imported template to a host and enjoy!</li>
</ol>
