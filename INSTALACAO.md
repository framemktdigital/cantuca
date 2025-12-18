# 🚀 Instruções de Deploy - Link Bio Cantuca Brasero & Bar

> Guia completo para enviar alterações do Link Bio para produção

---

## 📋 Informações do Projeto

**Projeto:** Link Bio - Cantuca Brasero & Bar
**Tipo:** HTML estático (Link na Bio)
**GitHub:** framemktdigital/bio-cantuca (a ser criado)

### Estrutura do Projeto
```
bio-cantuca/
├── index.html       # Página principal
├── logo.png         # Logo do Cantuca Brasero & Bar
├── vercel.json      # Configuração Vercel
└── README.md        # Documentação
```

**Total:** 4 arquivos (HTML puro, sem dependências)

---

## 🎯 Opções de Hospedagem

### Opção 1: Vercel (Recomendado para Bio)

**Deploy automático via GitHub:**
1. O repositório já está conectado ao Vercel (ver `vercel.json`)
2. Push para branch `main` faz deploy automático
3. URL gerada automaticamente

**Deploy manual via CLI:**
```bash
cd /home/ubuntu/projetos/bio-cantuca
vercel --prod
```

### Opção 2: Servidor Hostinger

Se precisar hospedar em um dos servidores Hostinger, veja as opções abaixo.

---

## 🔍 Identificar Servidor de Hospedagem

**Verificar onde está hospedado atualmente:**

### Servidor ATLAS (147.79.84.132)
```bash
sshpass -p 'c="INPNs1' ssh -p 65002 -o StrictHostKeyChecking=no u805019072@147.79.84.132 "find domains -name '*canto*' -o -name '*bio*' 2>/dev/null"
```

### Servidor PHOENIX (147.79.92.117)
```bash
sshpass -p 'q:jbKuf&3Q' ssh -p 65002 -o StrictHostKeyChecking=no u171618401@147.79.92.117 "find domains -name '*canto*' -o -name '*bio*' 2>/dev/null"
```

### Servidor ICARUS (212.1.209.172)
```bash
sshpass -p 'k2J^@eLcCxkoq2|>q+_4/Bs7W@aPN~' ssh -p 65002 -o StrictHostKeyChecking=no u935603021@212.1.209.172 "find domains -name '*canto*' -o -name '*bio*' 2>/dev/null"
```

### Servidor MAGNUS (185.239.210.85)
```bash
sshpass -p 'dP.oUB;lcFIR_=)%0FVvNMPj<z&eYW' ssh -p 65002 -o StrictHostKeyChecking=no u912908925@185.239.210.85 "find domains -name '*canto*' -o -name '*bio*' 2>/dev/null"
```

---

## 🚀 Deploy para Servidor Hostinger

**IMPORTANTE:** Primeiro identifique o servidor correto usando os comandos acima.

### Template de Deploy (Ajustar conforme servidor)

**Exemplo para Servidor ATLAS:**
```bash
# Dry-run (simular)
sshpass -p 'c="INPNs1' rsync -avz --dry-run --progress -e "ssh -p 65002 -o StrictHostKeyChecking=no" \
  --exclude='.git' \
  --exclude='.gitignore' \
  --exclude='README.md' \
  --exclude='vercel.json' \
  /home/ubuntu/projetos/bio-canto/ \
  u805019072@147.79.84.132:domains/[DOMINIO]/public_html/

# Deploy real
sshpass -p 'c="INPNs1' rsync -avz --progress -e "ssh -p 65002 -o StrictHostKeyChecking=no" \
  --exclude='.git' \
  --exclude='.gitignore' \
  --exclude='README.md' \
  --exclude='vercel.json' \
  /home/ubuntu/projetos/bio-canto/ \
  u805019072@147.79.84.132:domains/[DOMINIO]/public_html/
```

**Exemplo para Servidor PHOENIX:**
```bash
# Dry-run (simular)
sshpass -p 'q:jbKuf&3Q' rsync -avz --dry-run --progress -e "ssh -p 65002 -o StrictHostKeyChecking=no" \
  --exclude='.git' \
  --exclude='.gitignore' \
  --exclude='README.md' \
  --exclude='vercel.json' \
  /home/ubuntu/projetos/bio-canto/ \
  u171618401@147.79.92.117:domains/[DOMINIO]/public_html/

# Deploy real
sshpass -p 'q:jbKuf&3Q' rsync -avz --progress -e "ssh -p 65002 -o StrictHostKeyChecking=no" \
  --exclude='.git' \
  --exclude='.gitignore' \
  --exclude='README.md' \
  --exclude='vercel.json' \
  /home/ubuntu/projetos/bio-canto/ \
  u171618401@147.79.92.117:domains/[DOMINIO]/public_html/
```

---

## 📝 Git e GitHub

### Verificar status do repositório
```bash
cd /home/ubuntu/projetos/bio-canto
git status
```

### Fazer commit das alterações
```bash
cd /home/ubuntu/projetos/bio-canto

# Adicionar arquivos alterados
git add .

# Commit com mensagem
git commit -m "Atualizar conteúdo do Link Bio

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>"

# Push para GitHub
git push origin main
```

### Atualizar do repositório remoto
```bash
cd /home/ubuntu/projetos/bio-canto
git pull origin main
```

---

## ✅ Checklist Antes do Deploy

- [ ] Testar página localmente (abrir index.html no navegador)
- [ ] Verificar se logo.jpg está presente
- [ ] Verificar links de redes sociais
- [ ] Verificar links do WhatsApp
- [ ] Confirmar servidor de destino correto
- [ ] Fazer dry-run antes do deploy real
- [ ] Se usar Vercel, apenas fazer push no GitHub
- [ ] Testar site após deploy
- [ ] Verificar responsividade mobile

---

## 🛠️ Comandos Úteis

### Abrir arquivo localmente
```bash
# Linux/WSL
xdg-open /home/ubuntu/projetos/bio-canto/index.html

# Ou copiar para área pública e acessar via navegador
```

### Verificar tamanho do projeto
```bash
du -sh /home/ubuntu/projetos/bio-canto/
```

### Contar linhas de código
```bash
wc -l /home/ubuntu/projetos/bio-canto/index.html
```

---

## 🔗 Links Importantes

**Repositório GitHub:** https://github.com/framemktdigital/bio-canto

**Tecnologias:**
- HTML5
- CSS3 (inline no HTML)
- JavaScript Vanilla
- Font Awesome 6.5.1
- Google Fonts (Poppins)

**Características:**
- 🎨 Design moderno (preto, dourado, vinho)
- 📱 Totalmente responsivo
- 🚀 Performance (HTML puro)
- 📊 Google Tag Manager integrado
- ♿ Acessível (aria-labels)
- 🎬 Animações suaves

---

## 🌐 Informações dos Servidores

### 🏛️ ATLAS
- IP: 147.79.84.132
- Porta: 65002
- Usuário: u805019072
- Senha: c="INPNs1

### 🔥 PHOENIX
- IP: 147.79.92.117
- Porta: 65002
- Usuário: u171618401
- Senha: q:jbKuf&3Q

### 🪽 ICARUS
- IP: 212.1.209.172
- Porta: 65002
- Usuário: u935603021
- Senha: k2J^@eLcCxkoq2|>q+_4/Bs7W@aPN~

### ⚔️ MAGNUS
- IP: 185.239.210.85
- Porta: 65002
- Usuário: u912908925
- Senha: dP.oUB;lcFIR_=)%0FVvNMPj<z&eYW

---

## 🚨 Atenção

- Projeto é **HTML puro** - sem build necessário
- Se hospedado no Vercel, deploy é automático via GitHub
- Se hospedado no Hostinger, use rsync conforme templates acima
- Sempre faça dry-run antes do deploy real
- Verifique se está enviando para o domínio/servidor correto
- Não envie arquivos desnecessários (.git, README.md, vercel.json)

---

**Criado em:** 2025-11-21
**Última atualização:** 2025-11-21
**GitHub:** framemktdigital/bio-canto
