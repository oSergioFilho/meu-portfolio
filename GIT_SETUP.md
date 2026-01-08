# 📚 Como configurar Git e GitHub para este projeto

## Passo 1: Instalar Git

1. Baixe o Git para Windows: https://git-scm.com/download/win
2. Instale seguindo o instalador (pode deixar todas as opções padrão)
3. **IMPORTANTE**: Após instalar, **feche e reabra o terminal/PowerShell** para que o Git funcione

## Passo 2: Configurar Git (primeira vez)

Abra o PowerShell e execute:

```powershell
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

## Passo 3: Criar repositório no GitHub

1. Acesse https://github.com e faça login
2. Clique no botão "+" no canto superior direito
3. Selecione "New repository"
4. Nome do repositório: `meu-portfolio` (ou o nome que preferir)
5. Deixe como **Público** ou **Privado** (sua escolha)
6. **NÃO marque** "Add a README file" (já temos um)
7. Clique em "Create repository"

## Passo 4: Inicializar Git no projeto

No PowerShell, na pasta do projeto, execute:

```powershell
# Navegar para a pasta do projeto (se necessário)
cd "C:\Users\sergi\Downloads\Strategy\Strategy"

# Inicializar repositório Git
git init

# Adicionar todos os arquivos
git add .

# Fazer primeiro commit
git commit -m "Initial commit: Portfólio personalizado de desenvolvedor"

# Adicionar o repositório remoto do GitHub (SUBSTITUA 'seu-usuario' e 'meu-portfolio')
git remote add origin https://github.com/seu-usuario/meu-portfolio.git

# Renomear branch para main (se necessário)
git branch -M main

# Fazer push para o GitHub
git push -u origin main
```

## Próximos commits

Para salvar alterações futuras:

```powershell
git add .
git commit -m "Descrição das alterações"
git push
```

## 🆘 Problemas comuns

### Erro: "git não é reconhecido"
- Certifique-se de que o Git foi instalado
- Feche e reabra o PowerShell/terminal
- Reinicie o computador se necessário

### Erro de autenticação no push
- O GitHub não aceita mais senha via HTTPS
- Você precisará criar um Personal Access Token:
  1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
  2. Generate new token (classic)
  3. Selecione permissões: `repo`
  4. Use o token como senha ao fazer push

### Alternativa: GitHub Desktop
Se preferir uma interface gráfica, instale o GitHub Desktop:
https://desktop.github.com/
