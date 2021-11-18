# Installing Docker with OpenVAS/Greenbone vulnerability scanner

## Setup

**Welcome to how to install Docker**
<p>This is how to install Docker and OpenVAS vulnerability scanner. . </p>
<p>Open your Ubuntu VM and open terminal.</p>

**Apt Update**
<p>Update all the reposititories.</p>
<pre><code> sudo apt-get update</code></pre>

**Apt Upgrade**
<p>Ugrade all the reposititories.</p>
<pre><code> sudo apt-get upgrade</code></pre>

**Install Docker**
<p>Install docker after update.</p>
<pre><code> sudo apt-get install docker.io</code></pre>

**Check Status**
<p>Check if docker is running</p>
<pre><code> sudo service docker status</code></pre>

**If inactive, run this**
<p>Run if not running.</p>
<pre><code>sudo service docker start</code></pre>


**Install Container for OpenVAS**
<p>Install container to run application</p>
<pre><code>sudo docker run -d -p 443:443 --name openvas mikesplain/openvas</pre></code>


**Open Local Host**
<p>Container is now local so open.</p>
<pre><code>https://localhost/</pre></code>

**Login to OpenVAS**
<p>Login to OpenVAS</p>
<pre><code>login: admin password: admin</pre></code>

**Run Vulnerability Scan**
<p>Open dashboard and hover over "Scans" and click "Task". Once it loads click the star icon and choose to create Vulnerability Scan.</p>

**OUTPUT**
![scan](./openvas.PNG)  

**How to create a docker-compose.yml file**
<pre><code>docker run -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock:ro --restart always --log-out max-size=1g nginx</pre></code>

**OUTPUT**
![yml](./yml.PNG)
