# Introduction

# Setup

To encrypt the file, define the ARN of your KMS key in .sops.yaml.
Then, do:

```bash
$ aws eks \
    --region <region> \
    update-kubeconfig \
    --name <cluster-name> \
    --profile <profile>
$ export AWS_PROFILE=<aws-profile>
$ helm secrets enc setup/agent-config/secrets.yaml
```

Then, modify the controller ARN value using your ARN role.

# Services

To get the AWS Load Balancer URL, do:

```bash
kubectl get ingress --all-namespaces -o wide
```
