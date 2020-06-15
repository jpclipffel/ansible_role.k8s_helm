# IaC / Ansible / Roles / K8S Helm

Install Helm on Kubernetes clusters.

## Usage

Include the role in your playbook using the `include_role` module (do not specify the `file` attribute):

```yaml
include_role:
  name: k8s_helm
```

Do not forget to set the common `k8s_` variables:

* `k8s_primary_master_name`
* `k8s_node_type`

## Tags

| Tag      | Description             |
|----------|-------------------------|
| `setup`  | Install or upgrade Helm |
| `remove` | Uninstall Helm          |

## Variables

Role variables are prefixed with `k8s_helm_`.

| Variable                | Type     | Required | Defaut        | Description                     |
|-------------------------|----------|----------|---------------|---------------------------------|
| `k8s_helm_version`      | `string` | No       | `3.0.3`       | Helm version string             |
| `k8s_helm_distribution` | `string` | No       | `linux-amd64` | Helm distribution (OS-specific) |

## Tasks sequence

```text
main.yml
```
