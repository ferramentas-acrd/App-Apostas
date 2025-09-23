# Apps de Apostas

Plataforma completa para comparar e baixar os melhores aplicativos de apostas esportivas do Brasil. Reviews detalhados, tutoriais e bônus exclusivos.

## 🚀 Tecnologias

- **Frontend:** Astro 5.13.10 + TypeScript + Tailwind CSS
- **CMS:** Strapi 5
- **Database:** SQLite (desenvolvimento) / MySQL (produção)
- **Infrastructure:** AWS EC2, Cloudflare, Nginx

## 📁 Estrutura do Projeto

```
App-Apostas/
├── frontend/          # Astro Application
│   ├── src/
│   │   ├── pages/     # Astro Pages
│   │   ├── components/# Astro Components
│   │   ├── layouts/   # Page Layouts
│   │   └── lib/       # Utilities & API
│   └── package.json
├── cms/               # Strapi CMS
│   ├── src/
│   │   └── api/       # Content Types
│   └── package.json
└── README.md
```

## 🌟 Funcionalidades

### Páginas Implementadas
- **Homepage** (`/`) - Página inicial com comparação de apps
- **Top Apps** (`/top-apps`) - Ranking dos melhores aplicativos
- **Reviews** (`/reviews`) - Análises detalhadas de cada app
- **Tutoriais** (`/tutoriais`) - Guias de instalação e uso

### Recursos
- Design responsivo baseado no Figma
- Comparação interativa de apps de apostas
- Sistema de reviews e avaliações
- Filtros por categoria (iOS, Android, Esportes)
- Tabela comparativa de recursos
- Tutoriais passo a passo
- SEO otimizado

## 🛠️ Desenvolvimento Local

### Pré-requisitos
- Node.js 20.19.4+
- npm ou yarn

### Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/ferramentas-acrd/App-Apostas.git
cd "App-Apostas"
```

2. **Instale dependências:**
```bash
# Frontend
cd frontend
npm install

# CMS
cd ../cms
npm install
```

3. **Configure variáveis de ambiente:**
```bash
# Em frontend/.env.local
NEXT_PUBLIC_STRAPI_URL=http://localhost:1337
STRAPI_API_TOKEN=your_token_here
```

4. **Inicie os serviços:**
```bash
# Terminal 1 - Strapi CMS
cd cms
npm run develop

# Terminal 2 - Frontend
cd frontend
npm run dev
```

### URLs de Desenvolvimento
- **Frontend:** http://localhost:4321
- **Strapi Admin:** http://localhost:1337/admin

## 📊 Content Types (Strapi)

- **Articles** - Notícias e artigos
- **Categories** - Categorias de conteúdo
- **Tags** - Tags para organização
- **Teams** - Informações de times

## 🎨 Design

O projeto segue a identidade visual definida no Figma, com:
- Cores principais: Vermelho (#dc2626) e Preto
- Tipografia: Inter
- Layout responsivo e moderno
- Componentes baseados no Tailwind CSS

## 🚀 Deploy

### Produção
- **Frontend:** Vercel/AWS EC2
- **CMS:** AWS EC2 com Nginx
- **Database:** MySQL
- **CDN:** Cloudflare

### Configuração de Produção
```bash
# Build frontend
npm run build

# Build Strapi
npm run build
npm run start
```

## 📝 Páginas Planejadas

- `/` - Homepage
- `/apostas/` - Categoria Apostas
- `/palpites/` - Categoria Palpites  
- `/apostas/melhores-casas-de-apostas/` - Artigo específico
- `/times/cruzeiro/` - Página do time

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## 📞 Suporte

Para suporte e dúvidas, entre em contato através dos issues do GitHub.

---

**Diário do Futebol** - O portal mais completo de esportes e apostas do Brasil 🇧🇷⚽