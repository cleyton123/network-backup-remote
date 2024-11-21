# network-backup-remote
  Este é um projeto de backup remoto para um servidor onde é utilisado as seguintes ferramentas: rsync e o ssh. irei apresentar as imagens do mesmo e explicar o que foi feito em cada.
  
  ![Untitled design(2)](https://github.com/user-attachments/assets/b26c7619-19c3-4232-a723-1fe37bc1be09)

Nesta imagem foi criado trÊs pastas "pai" e seus respectivos "filhos" dentro do diretório backup_local.em seguida com o comando "nano script_sh" dentro do diretório script foi criado um script para automatizar o processo de backup.

![Untitled design (cópia)](https://github.com/user-attachments/assets/ce42099f-8a45-43f9-a3c2-2b55d8dab25f)


A imagem mostra um script Bash que realiza um backup de arquivos de um diretório local para um servidor remoto utilizando rsync. 
Este script automatiza o processo de backup de arquivos locais para um servidor remoto:

    Cria um diretório único no servidor remoto com base na data e hora.
    Transfere os arquivos usando rsync com compressão e preservação de atributos.
    Exibe uma mensagem indicando o sucesso ou a falha da operação.

![Untitled design(1)](https://github.com/user-attachments/assets/e91737c8-3db0-45c4-8ffb-f6dfd0baec77)



    Após a criação do script a imagem a acima mostra a conexão com o servidor via ssh e o diretório de destino que se encontra vazio. Dando continuidade vemos que depois de desconectar do servidor é realizado a execução do script com sucesso na máquina local.

    ![Untitled design](https://github.com/user-attachments/assets/741a3348-cf10-48fc-a9e7-be989a0a2043)

Novamente é acessado via ssh o servidor e é possível verificar a criação de uma pasta  timestamp (backup_2024-11-21_14-24-25) conforme o script. dentro desta nova pasta encontra-se as mesmas pastas e subpastas da máquina local.
Logo o script esta funcionando corretamente.
