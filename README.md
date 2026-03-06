
***

## Vector Role README.md

**roles/vector/README.md**
```markdown
# Vector Role

Installs Vector log shipper and configures it to ship logs to ClickHouse.

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `vector_version` | `0.53.0` | Vector package version |
| `vector_config_path` | `/etc/vector/vector.yaml` | Vector config file path |
| `clickhouse_server_ip` | `192.168.10.1` | ClickHouse server IP |

## Requirements

- Debian/Ubuntu systems
- ClickHouse server accessible

## Example Playbook

```yaml
***
- hosts: vector
  become: true
  vars:
    clickhouse_server_ip: "192.168.10.1"
  roles:
    - role: vector
