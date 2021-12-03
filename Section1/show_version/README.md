# Show version

You need to update the hosts file : replace the "veos" host
with one to which you can log on with ssh.

Run ``ansible-playbook -i hosts show_version.yaml``.

# Show the full responses to a module invocation

This will show all of the responses, including
the bits that most people don't even exist.

Run ``ansible-playbook -i hosts show_all_responses.yaml``

# Multiple lines of commands

Run ``ansible-playbook -i hosts show_version_and_uptime.yaml``
