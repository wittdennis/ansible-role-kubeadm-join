# kubeadm_join

Ansible role to join a node to a kubeadm managed kubernetes cluster.

## Requirements

In order to generate join tokens the role tries to delegate the generation to a initialized control plane. This control plane has to be in a host group called `kubernetes_control_plane`.

## Role Variables

```yaml
# see: https://kubernetes.io/docs/reference/config-api/kubeadm-config.v1beta3/#kubeadm-k8s-io-v1beta3-JoinConfiguration
kubeadm_join_join_configuration: {} # defaults to empty
kubeadm_join_external_etcd: false # Set to true if an externally managed etcd is used
```

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: kubernetes_cluster
      roles:
         - { role: wittdennis.kubeadm_join }

## License

MIT
