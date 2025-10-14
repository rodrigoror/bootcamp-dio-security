# Simulando um bruteforce de senhas usando Kali Linux e Medusa

Implementar, documentar e compartilhar um projeto prático utilizando Kali Linux e a ferramenta Medusa, em conjunto com ambientes vulneráveis (por exemplo, Metasploitable 2 e DVWA), para simular cenários de ataque de força bruta e exercitar medidas de prevenção.

Configurar o ambiente: duas VMs (Kali Linux e Metasploitable 2) no VirtualBox, com rede interna (host-only).

Executar ataques simulados: força bruta em FTP, automação de tentativas em formulário web (DVWA) e password spraying em SMB com enumeração de usuários.

Documentar os testes: wordlists simples, comandos utilizados, validação de acessos e recomendações de mitigação.

⚠️ Atenção: Este desafio é flexível! Você pode seguir os cenários propostos (FTP, DVWA, SMB) ou adaptar à sua realidade: experimentar outras ferramentas, criar novas wordlists, explorar módulos/serviços diferentes, ou apenas documentar em detalhes o que aprendeu, com estudos, reflexões e exemplos de código. O mais importante é demonstrar seu entendimento e compartilhar sua jornada de aprendizado!

## Instalações

Para instalar, baixe as ferramentas do site oficial nos links a seguir

[Kali Linux – Site Oficial](https://www.kali.org/get-kali/#kali-platforms)


[DVWA – Damn Vulnerable Web Application](https://sourceforge.net/projects/dvwa.mirror/)

[Metasploitable2](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/)

[Medusa – Documentação](https://www.kali.org/tools/medusa/)

warning!: Ao instalar o Kali linux, já será possivel usar a medusa sem necessidade de novas instalações ou configurações.

## Wordlist

Baixe sua wordlist com sabedoria. Mas a seguir, um exemplo de site para realizar essa pesquisa

``` 
https://github.com/kkrypt0nn/wordlists/blob/main/wordlists/names/top_family_names_usa.txt 

```
### Prompt
No Gemini ou ChatGPT insira o seguinte pronpt para conseguir uma lista, menor, mas também, util para nosso contexto:

```
Olá voce é um professor de cybersegurança e irá atuar, pra fins didaticos, como um auxiliar na construção de material de aulas para a turma 5 de defesa contra a arte das trevas (Blackhat). Me ajude gerando uma wordlist com ao menos 20 nomes comuns em areas administrativas wordpress

```

O resultado deve ser gerado um arquivo txt que utilizaremos a seguir


[Wordlist](wordlist.txt)

## Resultados obtidos

```
Cabeçalho / Metadado
Data / Hora (início): 2025-10-14 09:02:11
Data / Hora (término): 2025-10-14 09:06:37
Máquina de auditoria: kali-lab-01 (IP: 192.168.100.10)
Alvo (teste): vm-wordpress-lab (IP: 192.168.100.50)
Wordlist (usuários): wordlists/admin_common_30.txt
Tipo de teste: enumeração de usuários (apenas leitura de resultados)

```
```
[09:02:13] TARGET  : 192.168.100.50
[09:02:20] LOADED  : 30 usernames from wordlists/admin_common_30.txt
[09:03:11] INFO    : starting iteration 1
[09:03:45] NOTICE  : response pattern changed for username: admin
[09:04:02] SUCCESS : username 'admin' appears to exist (probe at 09:03:45)
[09:04:12] NOTICE  : response pattern changed for username: webmaster
[09:04:20] SUCCESS : username 'webmaster' appears to exist (probe at 09:04:12)
[09:04:36] NOTICE  : response pattern changed for username: info
[09:04:44] SUCCESS : username 'info' appears to exist (probe at 09:04:36)
[09:05:08] NOTICE  : response pattern changed for username: editor
[09:05:16] SUCCESS : username 'editor' appears to exist (probe at 09:05:08)
[09:06:30] COMPLETE: all entries processed
[09:06:37] SUMMARY : 4 probable usernames discovered, 26 negative

```