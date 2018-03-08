# Docker PHP environment
Docker building for PHP development.

### Stack

- Apache 2
- Mysql(5.7)
- PHP (5.6)
- PHP (7.1)
- Magento 1.9.x
- Opencart 3.x


### Build

```
Example:
cd opencart/
$ docker-compose up --build
```
### Access via broser after build

```
localhost:8000/project-name/
```


### Requirements

- Docker 
- Docker compose
- Composer (optional)

### Composer

- Use composer to update included projects in project-name/volume/project-name/.
