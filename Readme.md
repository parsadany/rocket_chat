Rocket Chat Docker Compose file behind Nginx with Conf file.

usage:

# edit your docker-compose:

```nano docker-compose.yml```

then change hostname ( and ports if needed!)

# run your instance:

```docker-compose up -d```

# install nginx with:

```apt install nginx```

# move your conf file:

```cp nginx.conf /etc/nginx/sites-available/rocketchat.conf```

# edit your conf file and replace your server_name:

```nano /etc/nginx/sites-available/rocketchat.conf```

# make link to sites-enabled:

```ln -s /etc/nginx/sites-available/rocketchat.conf /etc/nginx/sites-enabled/rocketchat.conf```

# check you config:

```nginx -t```

# enable and restart nginx:

```systemctl enable nginx && systemctl restart nginx```

# check nignx:

```systemctl status nginx```

now you can browse your website with http.

for https follow the instructions to use let's encrypt or zerossl to obtain ssl certs and automatically edit your nginx conf and redirect your site to https.

all done. enjoy!
