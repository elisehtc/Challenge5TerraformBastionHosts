# Challenge5TerraformBastionHosts

J'ai exécuté les commandes suivantes pour créer la clé ssh
- ssh-keygen -t rsa -b 2048 -f mykeypair
- eval $(ssh-agent)
- ssh-add -k mykeypair

Ensuite, j'ai dû modifier le fichier provider.tf parce que les fichiers de HDaniels1991 sur GitHUb sont pour une version 12 de Terraform alors que la mienne est une version 14,
et puis j'ai adapté les variables pour que ça corresponde à la région que j'utilise.

Les instances ont bien été créés -> voir aws.jpg

J'ai modifié le fichier .ssh/config pour y ajouter les instances -> voir ssh.config.jpg

J'ai finalement réussi à me connecter à l'instance privée avec la commande ssh private-instance -> voir private_instance_connection.jpg
