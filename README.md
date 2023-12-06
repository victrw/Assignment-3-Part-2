# Included material

- backend binary, hello-server
- frontend, index.html
- nginx configuration file, hello.conf
- service file for backend, hello-server.service
- config for setting up servers, cloud-config.yml
- example curl commands for testing your server, curl.md


# Directories where the material should be stored

All file ownership should be changed to root unless specified otherwise.

## hello-server
```
/usr/local/bin
```
**Notes**: Change the file ownership to www-data since in hello.conf because user is set to www-data

## index.html
```
/var/www/my-site
```
**Note**: You will need to create the directory if it doesn't exist.

## hello.conf
```
/etc/nginx/sites-available
```
**Note**: Since you are storing it here, you have to create a symbolic link for it in the directory called:
```
/etc/nginx/sites-enabled
```
```
sudo ln -s /etc/nginx/sites-available/hello.conf /etc/nginx/sites-enabled/hello.conf@
```
The @ is just to differenetiate from the orginal.

## hello-server.service
```
/etc/systemd/system
```