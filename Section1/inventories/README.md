# Inventories

Here are four inventories to amuse you; two with just hostnames
and two with variables added in to spice it up a little.

You can verify any of them as valid inventories with
``ansible-inventory`` and its ``graph`` option.

An example command line is...

```
ansible-inventory --graph -i hosts.ini
```

## Inventory variables
If you want to see the inventory variables too, you
will need to add ``--vars`` to the command line.
