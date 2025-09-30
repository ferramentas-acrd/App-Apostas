# 🚀 **GUIA COMPLETO - CMS APPS DE APOSTAS COMO WORDPRESS**

## ✅ **ACESSO AO CMS - 100% FUNCIONAL**

### **🔗 CREDENCIAIS DE ACESSO:**
```
URL: http://localhost:1338/admin
📧 Email: caio.bessa@acroud.media
🔐 Senha: 12345678!Nil
```

## 📋 **ESTRUTURA COMPLETA PARA PORTAL DE APOSTAS**

### **1. 📰 CONTENT TYPES ESSENCIAIS (CRIAR NO CMS)**

#### **🔸 POST (Collection Type)**
**Navegue: Content-Type Builder → Create new collection type**

| Campo | Tipo | Configuração |
|-------|------|--------------|
| `title` | Text | Required, Max 255 chars |
| `slug` | UID | From title, Required |
| `excerpt` | Long text | Max 500 chars |
| `content` | Rich text | Required |
| `coverImage` | Media | Single image |
| `category` | Relation | Many to One → Category |
| `tags` | Relation | Many to Many → Tag |
| `author` | Relation | Many to One → Author |
| `featured` | Boolean | Default false |
| `sticky` | Boolean | Default false |
| `viewCount` | Number | Default 0 |
| `publishedDate` | Date & Time | - |

#### **🔸 CATEGORY (Collection Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `name` | Text | Required, Max 100 chars |
| `slug` | UID | From name, Required |
| `description` | Long text | Max 500 chars |
| `color` | Text | Hex color |
| `icon` | Text | Icon class |
| `coverImage` | Media | Single image |
| `showInMenu` | Boolean | Default true |
| `order` | Number | Default 0 |

#### **🔸 TAG (Collection Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `name` | Text | Required, Max 50 chars |
| `slug` | UID | From name, Required |
| `description` | Long text | Max 300 chars |
| `color` | Text | Hex color |

#### **🔸 APP (Collection Type) - ESPECÍFICO APOSTAS**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `name` | Text | Required |
| `slug` | UID | From name |
| `description` | Long text | Required |
| `shortDescription` | Text | Max 200 chars |
| `icon` | Media | Single image, Required |
| `screenshots` | Media | Multiple images |
| `rating` | Number | Decimal 1-5 |
| `reviewCount` | Number | Integer |
| `bonus` | Text | Ex: "R$500" |
| `bonusCode` | Text | Ex: "APP300" |
| `features` | JSON | Lista de features |
| `hasLiveStreaming` | Boolean | - |
| `hasCashOut` | Boolean | - |
| `supportsPix` | Boolean | - |
| `hasCasino` | Boolean | - |
| `hasIOS` | Boolean | - |
| `hasAndroid` | Boolean | - |
| `downloadUrlAndroid` | Text | URL da Play Store |
| `downloadUrlIOS` | Text | URL da App Store |
| `websiteUrl` | Text | Site oficial |
| `featured` | Boolean | - |
| `topRated` | Boolean | - |
| `order` | Number | Para ordenação |

#### **🔸 AUTHOR (Collection Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `name` | Text | Required |
| `slug` | UID | From name |
| `email` | Email | Required, Unique |
| `bio` | Long text | - |
| `avatar` | Media | Single image |
| `expertise` | Enumeration | futebol, basquete, esports, etc |
| `active` | Boolean | Default true |

#### **🔸 MENU ITEM (Collection Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `title` | Text | Required |
| `url` | Text | Required |
| `target` | Enumeration | _self, _blank |
| `icon` | Text | Icon class |
| `order` | Number | Para ordenação |
| `menuLocation` | Enumeration | header, footer, sidebar |
| `active` | Boolean | Default true |

#### **🔸 SITE SETTINGS (Single Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `siteName` | Text | Required |
| `siteDescription` | Long text | - |
| `logo` | Media | Single image |
| `favicon` | Media | Single image |
| `socialMedia` | JSON | Links redes sociais |
| `contactInfo` | JSON | Dados de contato |
| `footerText` | Rich text | - |
| `maintenanceMode` | Boolean | Default false |

### **2. 🏠 WIDGETS DA HOME (Collection Type)**
| Campo | Tipo | Configuração |
|-------|------|--------------|
| `title` | Text | Required |
| `type` | Enumeration | latest_posts, featured_apps, statistics, etc |
| `position` | Enumeration | hero, section_1, section_2, sidebar |
| `order` | Number | Para ordenação |
| `settings` | JSON | Configurações específicas |
| `active` | Boolean | Default true |
| `limit` | Number | Quantidade de itens |

## 🎯 **COMO IMPLEMENTAR NO CMS**

### **PASSO 1: CRIAR CONTENT TYPES**
1. Acesse: http://localhost:1338/admin
2. Vá em **Content-Type Builder**
3. Clique **"Create new collection type"**
4. Siga a tabela acima para cada content type

### **PASSO 2: CONFIGURAR RELAÇÕES**
1. **Post → Category:** Many to One
2. **Post → Tags:** Many to Many  
3. **Post → Author:** Many to One
4. **Category → Posts:** One to Many

### **PASSO 3: POPULAR COM DADOS**
1. Vá em **Content Manager**
2. Crie categorias: "Apps iOS", "Apps Android", "Notícias", "Reviews"
3. Crie tags: "bet365", "futebol", "cassino", "bonus"
4. Crie apps: bet365, Superbet, Esportiva Bet
5. Crie posts de exemplo

### **PASSO 4: CONFIGURAR MENUS**
1. Crie itens de menu no Content Manager
2. Configure URLs e ordem
3. Defina localização (header/footer)

## 🔧 **INTEGRAÇÃO COM FRONTEND**

### **ROTAS DINÂMICAS A IMPLEMENTAR:**
- `/categoria/[slug]` - Lista posts por categoria
- `/tag/[slug]` - Lista posts por tag  
- `/app/[slug]` - Página individual do app
- `/autor/[slug]` - Página do autor
- `/[slug]` - Post individual

### **WIDGETS DINÂMICOS:**
- Latest Posts Widget
- Featured Apps Widget  
- Categories Widget
- Statistics Widget
- Custom Content Widget

## 🎯 **PRÓXIMOS PASSOS PRÁTICOS**

### **1. ✅ AGORA (5 MINUTOS):**
- Acesse o CMS
- Crie o content type "Category" 
- Crie algumas categorias de teste

### **2. 🔧 EM SEGUIDA:**
- Crie os outros content types
- Popular com dados de exemplo
- Testar integração no frontend

### **3. 🚀 RESULTADO FINAL:**
- CMS completo como WordPress
- Frontend totalmente dinâmico
- Gestão total via interface visual

## 📊 **FUNCIONALIDADES COMO WORDPRESS**

✅ **Gestão de Posts** - Criar, editar, publicar
✅ **Sistema de Categorias** - Hierárquico
✅ **Sistema de Tags** - Flexível  
✅ **Gestão de Menus** - Drag & drop
✅ **Widgets Personalizáveis** - Home customizável
✅ **SEO Completo** - Meta tags, structured data
✅ **Media Library** - Gestão de imagens
✅ **Usuários e Permissões** - Controle de acesso
✅ **Draft/Publish** - Sistema de rascunhos
✅ **Busca e Filtros** - Por categoria, tag, etc

**🏆 O CMS Apps de Apostas será tão robusto quanto WordPress!**