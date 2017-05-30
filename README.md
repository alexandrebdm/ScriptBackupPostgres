# ScriptBackupPostgres

Script shell para criar um Backup do PostGres.

A primeira linhha descreva a linguangem do script(bash, sh, htm, etc).

>#!/bin/bash

confirma senha:

>export PGPASSWORD = "senhaPostgres"

Utiliza o comando pg_dump para realizar backup e pg_restore para para o postgres reconhecer dados do backup

pg_dump -U (usuario) -h (localhost) -O -q -b -F c (banco) > (arquivo).backup

Onde os nomes em parenteses devem ser preenchidas por locais respectivos.

>pg_dump -U postgres -h localhost -O -o -b -F c floricultura > floricultura_backup.backup

Para restaurar o arquivo:
pg_restore -U postgres -h floricultura -d NOME_BANCO_DADOS NOME_DO_BACKUP.backup

Realizar a execução do arquivo Shell.

OBS: Incluir as variáveis de ambiente "pg_dump" e "pg_restore" do postgres. Caso o sistema não encontre os comandos.
