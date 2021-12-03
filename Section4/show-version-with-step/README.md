# Show version with `--step`

You need to update the hosts file : replace the "veos" host
with one to which you can log on with ssh.

Run ``ansible-playbook -i hosts --step show-version.yaml``
and follow the prompts.

