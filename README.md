# sleif.letsencrypt_nginx_container

This role runs an Nginx-based lets-encrypt stack on Podman.

## Requirements

na

## Role Variables

- container_storage_dir_base (/srv)
- nameserver_fallback_needed (true, in case you want local network independent DNS, for example, Pihole on the same container host)

## Dependencies

Enterprise Linux version 9

## Example Playbook

    - hosts: "server"
      user: root
      roles:
        - { role: sleif.letsencrypt_nginx_container, tags: "letsencrypt_nginx_container" }

## License

MIT

## Author Information

Created in 2023 by Sebastian Berthold
