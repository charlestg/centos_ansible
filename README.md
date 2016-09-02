## RUN

```
alias ansible='docker run --rm -it --name ansible -v `pwd`:/data ansible_console ansible'

docker run --rm -it \
    --name ansible \
    -e ANSIBLE_HOST_KEY_CHECKING=False \
    -v `pwd`:/data \
    ansible_console ansible --help
```

## Example

```
ansible --help
ansible all -i hosts -m shell -a 'echo hello world'
ansible all -i "10.10.10.10," -m shell -a 'echo hello world'
```