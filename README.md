# 🔐 Simulação de Ataques de Força Bruta com Kali Linux e Medusa

## 📌 Sobre o Projeto

Este repositório documenta a implementação prática de um ambiente controlado para simulação de ataques de força bruta utilizando **Kali Linux**, **Medusa** e máquinas vulneráveis como **Metasploitable 2** e **DVWA**.

O objetivo é demonstrar, na prática, como funcionam ataques de autenticação, como identificá-los e principalmente como mitigá-los.

> ⚠️ Todos os testes foram realizados em ambiente isolado e controlado para fins educacionais.

---

## 🎯 Objetivos de Aprendizagem

Ao concluir este projeto, fui capaz de:

- Compreender ataques de força bruta em diferentes serviços (FTP, Web, SMB);
- Utilizar o Kali Linux e a ferramenta Medusa para auditoria de segurança;
- Documentar processos técnicos de forma clara e estruturada;
- Identificar vulnerabilidades comuns e propor medidas de mitigação;
- Utilizar o GitHub como portfólio técnico para compartilhamento de conhecimento.

---

## 🖥️ Ambiente de Laboratório

### 📦 Infraestrutura

- 2 Máquinas Virtuais no VirtualBox:
  - Kali Linux Atualizado para a versão estável mais recente (máquina atacante)
  - Metasploitable 2 (máquina vulnerável)
- Rede configurada como **Modo Bridge** (o modo host-only não estava funcionando)
- DVWA instalado na Metasploitable

### 🔎 Ferramentas Utilizadas

- Kali Linux
- Medusa
- Wordlists personalizadas (comando echo)
- VirtualBox
- Navegador Web (para DVWA)

---

# 🌐 Protocolos Testados e Portas Utilizadas

Durante os testes práticos, foram analisados os seguintes protocolos e suas respectivas portas padrão:

## 🔹 FTP (File Transfer Protocol)

- **Protocolo:** FTP  
- **Porta TCP padrão:** 21  
- **Finalidade:** Transferência de arquivos em rede  

### ⚠️ Observação
O FTP transmite credenciais em texto claro, o que o torna vulnerável a interceptação e ataques de força bruta. Por esse motivo, recomenda-se a utilização de **SFTP** ou **FTPS** em ambientes produtivos.

---

## 🔹 SMB (Server Message Block)

- **Protocolo:** SMB  
- **Porta TCP padrão:** 445  
- **Finalidade:** Compartilhamento de arquivos e recursos em redes Windows  

### ⚠️ Observação
O SMB é frequentemente alvo de ataques como:
- Força bruta
- Password spraying
- Enumeração de usuários

É fundamental aplicar políticas de senha forte, restrições de acesso e monitoramento constante.

---

## 📌 Resumo Técnico

| Protocolo | Porta TCP | Tipo de Teste Realizado |
|-----------|-----------|--------------------------|
| FTP       | 21        | Força bruta de credenciais |
| SMB       | 445       | Password spraying |


---

# 📚 Wordlists Utilizadas nos Testes

Durante os cenários de ataque, foram utilizadas wordlists simples e controladas, criadas para fins educacionais. O objetivo foi simular más práticas comuns de senha e demonstrar a eficácia de ataques automatizados.

---

## 🔹 Ataque ao FTP

Foram utilizados dois arquivos de dicionário:

### 📄 users.txt

user
msfadmin
admin
root

### 📄 pass.txt

123456
password
qwerty
msfadmin


## 🔹 Ataque ao SMB

Foram utilizados dois arquivos de dicionário:

### 📄 smb_users.txt

user
msfadmin
service

### 📄 senhas_spray.txt

password
123456
Welcome123
msfadmin




