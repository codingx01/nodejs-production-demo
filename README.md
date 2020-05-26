# nodejs-production-demo

#Reverse Proxy setup
server {
    listen 80;
    server_name codingx.in;

    location / {
        proxy_pass http://localhost:3000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}

#Download Node
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
