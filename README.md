## RUN

```
alias ansible='docker run --rm -it --name ansible -v `pwd`:/data charlestg/centos_ansible ansible'

docker run --rm -it \
    --name ansible \
    -v `pwd`:/data \
    charlestg/centos_ansible ansible --help
```

## Example

```
ansible --help
ansible all -i hosts -m shell -a 'echo hello world'
ansible all -i "10.10.10.10," -m shell -a 'echo hello world'
```
