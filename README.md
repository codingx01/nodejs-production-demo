# nodejs-production-demo

#Reverse Proxy setup: 
<p><code>server {<br>
    listen 80; <br>
    server_name codingx.in;<br>
    location / {<br>
        proxy_pass http://localhost:3000;<br>
        proxy_set_header Host $host;<br>
        proxy_set_header X-Real-IP $remote_addr;<br>
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;<br>
        proxy_set_header X-Forwarded-Proto $scheme;<br>
    }<br>
}<br>
</code></p>

#Download Node: 
<p><code> curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh </code></p>
