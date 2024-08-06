# Problemas e Vulnerabilidades do FTP

Este documento explica as principais vulnerabilidades associadas ao FTP (File Transfer Protocol) e por que ele não é a melhor opção para a transferência segura de arquivos.

## Introdução

O FTP é um protocolo amplamente utilizado para a transferência de arquivos entre sistemas. No entanto, ele possui sérias deficiências de segurança, principalmente devido à sua transmissão de dados em texto simples. Isso expõe as informações sensíveis a diversos tipos de ataques.

## Problemas Principais

### Transmissão em Texto Claro

O FTP transmite todas as informações, incluindo credenciais de login e dados transferidos, sem criptografia. Isso significa que qualquer pessoa que possa interceptar o tráfego de rede pode ler essas informações. Ferramentas como tcpdump ou Wireshark podem ser usadas para capturar e visualizar dados sensíveis, como nomes de usuário, senhas e o conteúdo dos arquivos transferidos.

### Falta de Criptografia

A ausência de criptografia no FTP torna o protocolo vulnerável a vários tipos de ataques, incluindo:
- **Sniffing**: Captura do tráfego de rede para obter informações sensíveis.
- **Man-in-the-Middle (MitM)**: Ataques onde o invasor intercepta e possivelmente altera a comunicação entre o cliente e o servidor.

### Portas Padrão

O FTP utiliza portas padrão (21 para controle e 20 para dados), que são frequentemente alvos de ataques. A utilização dessas portas conhecidas facilita a tarefa de atacantes que tentam explorar vulnerabilidades específicas do protocolo FTP.

## Alternativas Seguras

Para uma transferência de arquivos mais segura, considere o uso de protocolos que oferecem criptografia e autenticação robustas, como:
- **SFTP (SSH File Transfer Protocol)**
- **FTPS (FTP Secure)**

Esses protocolos oferecem criptografia tanto para a comunicação quanto para os dados transferidos, protegendo suas informações contra interceptações e ataques.
