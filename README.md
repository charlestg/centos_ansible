## RUN

```
docker run --rm -it \
    --name ansible \
    -v `pwd`:/data \
    charlestg/centos_ansible ansible --help
```

## Alias

```
# Create Alias
alias ansible='docker run --rm -it --name ansible -v `pwd`:/data charlestg/centos_ansible ansible'

# Run with Alias
ansible --help
ansible all -i hosts -m shell -a 'echo hello world'
ansible all -i "10.10.10.10," -m shell -a 'echo hello world'
```
