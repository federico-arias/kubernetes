To encrypt the file, define the ARN of your KMS key in .sops.yaml.
Then, do:

```bash
$ export AWS_PROFILE=<aws-profile>
$ helm secrets enc setup/agent-config/secrets.yaml
```
