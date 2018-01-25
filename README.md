# rh-do407-notes

Ansible modules:
* command
* shell
* ping
* yum
* lineinfile
* copy
* service
* firewalld
* debug
* setup
* get_url
* uri
* file
* stat

Labs:
* 66 playbook
* 78 multiple play
* __85__ LAB 3
* 118 facts
* 132 inclusion
* __139__ LAB 4
* 155 flow control
* 162 handlers
* 174 tags
* 183 handling errors
* __193__ LAB 5
* 220 LAB 6
* 235 create roles
* 

Commands:
```
$ ansible-doc -l, --list  # List available modules
```

```
$ ansible-doc __stat__   # ansible-doc [options] [__module name__]

Output:
> STAT    (/usr/lib/python2.7/site-packages/ansible/modules/files/stat.py)

  Retrieves facts for a file similar to the linux/unix 'stat' command.

Options (= is mandatory):

- checksum_algorithm
        Algorithm to determine checksum of file. Will throw an error if the host is unable to use
        specified algorithm.
        (Choices: sha1, sha224, sha256, sha384, sha512)[Default: sha1]
...
```

```
$ ansible serverb.lab.example.com -m setup -a "filter=ansible_mem*"

serverb.lab.example.com | SUCCESS => {
    "ansible_facts": {
        "ansible_memfree_mb": 244, 
        "ansible_memory_mb": {
            "nocache": {
                "free": 339, 
                "used": 149
            }, 
            "real": {
                "free": 244, 
                "total": 488, 
                "used": 244
            }, 
            "swap": {
                "cached": 0, 
                "free": 0, 
                "total": 0, 
                "used": 0
            }
        }, 
        "ansible_memtotal_mb": 488
    }, 
    "changed": false
}
```

```
$ ansible-galaxy init --off-line -p roles/ abc.example
$ tree roles/

```

Notes:
* [Jinja2 is a templating engine for Python](http://jinja.pocoo.org/docs/2.10/)


Others:
* [new trading for a living pdf](https://drive.google.com/open?id=1mSqBpsROfCTxnJIa_5K8KnDMkYICnac9)
