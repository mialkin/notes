# Nginx

## Installing

### Ubuntu

```sh
sudo apt install nginx
```

### CentOS

Install nginx via YUM package manager.

```sh
sudo yum install nginx
```

## Configuring

Automatically start nginx on system boot.

```sh
sudo systemctl enable nginx
```

Start nginx right now.

```sh
sudo systemctl start nginx
```

## Reverse proxying

Switch to Ubuntu and CentOS folder containing configuration files.

```sh
cd /etc/nginx/conf.d
```

Create config file for domain.

```sh
sudo nano sub.domain.ru.conf
```

Example of a configuration file.

```text
server  {
  server_name sub.domain.com;
  location / {
    proxy_pass http://localhost:5001;
  }
}
```

Restart nginx.

```sh
sudo systemctl restart nginx
```