# Verifying connectivity with the ping module.

Just a reminder - this does NOT work on most network
equipment, but should work on servers.

```
ansible-playbook -i hosts ping.yaml
```

It should look like this:

```
$ ansible-playbook -i ./hosts ping.yaml

PLAY [A play to run the ping module] *********************************************************

TASK [Gathering Facts] ***********************************************************************
ok: [example.host.name]

TASK [A task to invoke the ping module] ******************************************************
ok: [example.host.name]

TASK [A task to print the output] ************************************************************
ok: [example.host.name] =>
  ping_results:
    changed: false
    failed: false
    ping: pong

PLAY RECAP ***********************************************************************************
example.host.name               : ok=3    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```

# Ping for an unknown host

If you want to see what happens when you try and
run a playbook against a non-existant host, try
this;

```
ansible-playbook -i hosts ping_unknown_host.yaml
```

(If you actually do have a host called "scapegoat" then you have bigger problems than a non-existant host...)

It should look like this:

```
$ ansible-playbook -i hosts ping_unknown_host.yaml
[WARNING]: Could not match supplied host pattern, ignoring: scapegoat

PLAY [A play to run the ping module] *********************************************************
skipping: no hosts matched

PLAY RECAP ***********************************************************************************
```
