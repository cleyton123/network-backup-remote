# Projeto de Backup Remoto para Servidor

 Este projeto implementa um sistema de backup remoto para servidores, utilizando as ferramentas rsync e ssh. O objetivo é automatizar o processo de cópia de arquivos do diretório local para um servidor remoto. Abaixo, são apresentadas as etapas do projeto, com imagens explicativas e descrição detalhada de cada passo.

 **Ferramentas Utilizadas**
 * rsync: Para transferência eficiente de arquivos, com compressão e preservação de atributos.
 * ssh: Para acesso remoto seguro ao servidor.

  **Etapas do Projeto**
  
  **1. Criação das Estruturas de Diretórios Locais**
  
  ![Untitled design(2)](https://github.com/user-attachments/assets/b26c7619-19c3-4232-a723-1fe37bc1be09)

* Foram criadas três pastas principais ("pai") e suas respectivas subpastas ("filhos") dentro do diretório backup_local.
* Em seguida, no diretório script, foi iniciado o desenvolvimento de um script Bash com o comando nano script_sh. Este script automatiza o processo de backup.

  **2. Desenvolvimento do Script de Backup**

![Untitled design (cópia)](https://github.com/user-attachments/assets/ce42099f-8a45-43f9-a3c2-2b55d8dab25f)


O script Bash criado realiza as seguintes ações:
* 1.**Criação de um diretório remoto único**: O script utiliza a data e hora atuais (timestamp) para criar pastas organizadas no servidor remoto.
* 2.**Transferência de arquivos**: O rsync é utilizado para enviar os arquivos do diretório local para o remoto, com opções para compressão e preservação de atributos.
* 3.**Mensagens de status**: Ao final, o script informa se o backup foi concluído com sucesso ou se houve alguma falha no processo.

  **3. Execução do Script e Verificação**

  **Conexão Inicial ao Servidor**

![Untitled design(1)](https://github.com/user-attachments/assets/e91737c8-3db0-45c4-8ffb-f6dfd0baec77)


* A imagem mostra a conexão com o servidor remoto via ssh.
* Observa-se que o diretório de destino (backup_remoto) estava vazio antes da execução do script.

  **Execução do Script**

  * Após desconectar do servidor, o script foi executado na máquina local com sucesso.

**4.Verificação do Backup no Servidor**

![Untitled design](https://github.com/user-attachments/assets/84026a78-d445-4271-a674-e56705f5a040)

    * Reacessando o servidor via ssh, é possível verificar a criação de uma pasta com o nome baseado no timestamp (ex.: backup_2024-11-21_14-24-25).
    * Dentro dessa pasta, encontram-se as mesmas estruturas de diretórios e arquivos presentes no diretório local.

    **Conclusão**

Com base nos resultados apresentados, o script de backup remoto está funcionando corretamente, automatizando a criação de backups organizados e seguros no servidor remoto.
O uso de ferramentas como rsync e ssh garante eficiência, confiabilidade e facilidade de manutenção para o processo.
