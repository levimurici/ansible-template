#Template de organização de projeto para utilização Vagrant + Ansible

1. É necessário mudar o usuário de o vagrant ID cat .vagrant/machines/{maquina}/{virtualbox}/{creator_uid}
2. É preciso criar as keys {mkdir ssh-keys && cd ssh-keys} {ssh-keygen -t rsa {/home/<user>/<folder>/ssh-keys/vagrant_id_rsa}}
3. É necessário copiar a ssh para permissão de acesso {ssh-copy-id -i vagrant_id_rsa.pub vagrant@(-- ip --)}
4. Mudar o caminho para o hosts achar a key
5. Depois de subidas as máquinas via vagrant up, é necessário executar o comando ansible-playbook -i hosts {playbook}.yml
