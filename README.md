# Redis

This role installs and configures a redis server. It allows to set all configuration variables supported by redis.


## Requirements

An apt- or pacman-based Linux distribution.


## Role Variables

This role seriously has a ton of variables. Instead of copying the defaults file here, look it up there. All variables from redis.conf are called exactly like they are called in the file but with redis_ prepended.
The 3 commands below are usable multiple times so theres an example syntax on how to do that.
```yml
redis_save:
    - "900 1"
    - "800 2"
redis_include:
    - "foo.conf"
    - "/etc/redis/bar.conf"
redis_rename_command:
    - "CONFIG b840fc02d524045429941cc15f59e41cb7be6c52"
```

## Example Playbook

```yml
- hosts: redis
  roles:
    - role: redis
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

 * [Fritz Otlinghaus (Scriptkiddi)](https://github.com/Scriptkiddi) _fritz.otlinghaus@stuvus.uni-stuttgart.de_
