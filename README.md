# Tiny Workshop for Lando
## Tiny Workshop Series for Summer 2023

### Presentation Materials
- [Google Presentation](https://docs.google.com/presentation/d/1RW61OzHkTS_MxJ30TQMQ4rzgLE9PhVBpWzDWnVrV9X0/edit?usp=sharing)

### Getting Started

Please follow the installation steps within the [Lando documentation](https://docs.lando.dev/getting-started/installation.html).

It should please be noted that the following are stated as requirements:

- macOS 11 or later
- Windows 10 Home or Pro version 21H2 or higher with the WSL 2 feature enabled
- Linux with kernel version 4.x or higher
- Docker Desktop
  - [macOS](https://docs.docker.com/desktop/install/mac-install/)
  - [Windows](https://docs.docker.com/desktop/install/windows-install/)
  - [Linux distributions](https://docs.docker.com/desktop/install/linux-install/)

### WordPress Example

#### Starting the Containers
```bash
$ cd ./src/wordpress
$ lando start
```

#### Inspecting the Containers
```bash
$ cd ./src/wordpress
$ lando list
```

#### Inspecting the Lando Configuration for the Containers
```bash
$ cd ./src/wordpress
$ lando info
```

#### Download WordPress Core
```bash
$ lando wp core download
```

#### Generate WordPress Config. File
```bash
$ lando wp config create \
  --dbname=wordpress \
  --dbuser=wordpress \
  --dbpass=wordpress \
  --dbhost=database
```

#### Install WordPress
```bash
$ lando wp core install \
  --url=https://wordpress-on-lando.lndo.site/ \
  --title="WordPress on Lando" \
  --admin_user=admin \
  --admin_password=password \
  --admin_email=admin@wordpress-on-lando.lndo.site
```

