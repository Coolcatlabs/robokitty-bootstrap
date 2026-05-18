# robokitty-bootstrap

Ansible playbook to bootstrap a Raspberry Pi for RoboKitty.

## Requirements

- Ansible 2.16+
- `community.general` collection

```bash
ansible-galaxy collection install -r requirements.yml
```

## Usage

```bash
ansible-playbook site.yml -i inventory/hosts.yml -K -vv
```

## Roles

| Role | Description |
|------|-------------|
| `common` | Base system configuration |
| `shell` | Shell environment and tools (starship, etc.) |
| `python` | Python environment and utilities to run robokitty application |

## Inventory

Update `inventory/hosts.yml` with the Pi's IP or hostname:

```yaml
all:
  hosts:
    raspberrypi:
      ansible_host: 192.168.0.x
      ansible_user: pi
```
