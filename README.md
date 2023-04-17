# sleif.letsencrypt_nginx_container

This role runs a nginx based letsencrypt stack on docker.

## Requirements

Use it on a machine setup with ansible role sleif.docker.

## Role Variables

- container_storage_dir_base (/srv)
- nameserver_fallback_needed (true, in case you want local network independent DNS, example pihole on same docker host)
- DOCKER_NETWORK_NAME (can be defined in sleif.docker)

## Dependencies

Enterprise Linux version 9
## Example Playbook

    - hosts: "server"
      user: root
      vars:
        DOCKER_NETWORK_NAME: 'custom_docker_network'
      roles:
        - { role: sleif.letsencrypt_nginx_container, tags: "letsencrypt_nginx_container" }

## License

MIT

## Author Information

Created in 2021 by Sebastian Berthold
