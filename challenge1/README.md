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


[Wordlist]
