# 🌎 Portfólio Multilíngue — Jeysson Zerpa

**Analista e Cientista de Dados | Business Intelligence | IA | Automação**

Portfólio pessoal em HTML, CSS e JavaScript puro, com suporte multilíngue (PT/ES/EN)
e um fundo 3D animado com **Three.js**. Sem build, sem framework, sem dependências
a instalar: o site é um ficheiro estático que qualquer servidor consegue publicar.

![Preview do Portfólio](og-image.png)

---

## 🧩 Estrutura real do projeto

```
📦 Sintesis-curricular
 ┣ 📜 index.html            # O site inteiro: marcação, estilos, dados PT/ES/EN e a cena 3D
 ┣ 🖼️ favicon.svg           # Ícone do separador
 ┣ 🖼️ apple-touch-icon.png  # Ícone para iOS (180×180)
 ┣ 🖼️ og-image.png          # Imagem de partilha em redes sociais (1200×630)
 ┣ 📜 robots.txt            # Indexação
 ┣ 📜 sitemap.xml           # Mapa do site
 ┣ ⚙️ vercel.json           # Cabeçalhos de segurança e de cache na Vercel
 ┗ 📜 README.md             # Este ficheiro
```

> O conteúdo dos três idiomas vive no objeto `Data`, dentro de `index.html`.
> As secções são geradas a partir dele — para editar o currículo, edita esse objeto.

---

## 🧠 Tecnologias

| Categoria | Ferramenta |
|---|---|
| Base | HTML5, CSS3, JavaScript (ES6+) |
| Tipografia | [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts |
| 3D | [Three.js](https://threejs.org/) r160 (CDN unpkg) |
| Design System | Variáveis CSS + Flexbox + Grid |
| Acessibilidade | `aria-*`, foco visível, `prefers-reduced-motion`, landmark `<main>` |
| SEO | Open Graph, Twitter Cards, JSON-LD (`Person`), sitemap |
| Alojamento | [Vercel](https://vercel.com/) (estático, sem configuração de build) |

Dependências externas: **Three.js** (CDN) e **Google Fonts**. Nenhuma outra.

---

## ✅ Funcionalidades

- **Três idiomas** — Português 🇧🇷, Espanhol 🇪🇸 e Inglês 🇺🇸, gerados a partir de JSON
- **Idioma automático** — detecta o do navegador e recorda a escolha entre visitas
- **Responsivo a sério** — cortes em 1100 / 900 / 720 / 560 / 380 px, com menu recolhível
- **Fundo 3D tolerante a falhas** — se o CDN ou o WebGL falharem, cai num fundo em CSS
- **Anima só quando é preciso** — pausa com o separador oculto ou o hero fora do ecrã
- **Táctil** — a cena reage ao dedo, não apenas ao rato
- **Acessível** — foco sempre visível, `lang` sincronizado, link para saltar ao conteúdo
- **Pronto para partilhar** — pré-visualização com imagem no LinkedIn e no WhatsApp
- **Imprimível** — folha de estilos dedicada para o currículo em papel

---

## ⚙️ Correr localmente

```bash
git clone https://github.com/jeyssonlza/Sintesis-curricular.git
cd Sintesis-curricular
npx serve          # depois abre http://localhost:3000
```

Abrir o `index.html` diretamente no navegador também funciona; só o `favicon`
e os caminhos absolutos (`/og-image.png`) é que não resolvem em `file://`.

---

## 🚀 Publicar na Vercel

O repositório é estático: **não precisa de build**.

1. Em [vercel.com/new](https://vercel.com/new), importa `jeyssonlza/Sintesis-curricular`
2. Framework Preset: **Other** · Build Command: *(vazio)* · Output Directory: `.`
3. Deploy

O `vercel.json` já trata dos cabeçalhos de segurança (CSP, `nosniff`,
`Referrer-Policy`, `Permissions-Policy`) e do cache: um ano para as imagens,
sempre revalidado para o HTML.

> **Antes de publicar**, troca `https://sintesis-curricular.vercel.app` pelo
> domínio real em quatro sítios: as metatags `canonical`/`og:url`/`og:image`
> e o JSON-LD no `index.html`, o `robots.txt` e o `sitemap.xml`.
> A Vercel publica a partir da branch `main`.

---

## 🔐 Boas práticas aplicadas

- `rel="noopener"` em todas as ligações externas
- `prefers-reduced-motion` respeitado — a cena 3D fica num único fotograma estático
- Dimensões do canvas ligadas ao hero, com `ResizeObserver` e `devicePixelRatio` limitado a 2
- A altura do header é medida em tempo real e alimenta o deslocamento das âncoras
- Conteúdo e apresentação separados: o currículo está todo no objeto `Data`

---

## 🧱 Próximos passos

- [ ] **Decidir o futuro da camada 3D.** A r160 é a última versão do Three.js que
      publica o build global `three.min.js` (e já avisa na consola que está
      obsoleto). As opções, medidas: manter a r160 (~163 KB gzip), migrar para
      ES Modules numa versão atual (~407 KB gzip) ou escrever a cena em WebGL
      puro (~5 KB). Subir o número da versão *não* funciona.
- [ ] Efeitos 3D e interatividade: parallax ao rolar, cartões com inclinação,
      revelação das secções, contadores animados
- [ ] Dar vida ao portfólio: ligações, imagens e métricas em cada projeto
- [ ] Currículo em PDF para descarregar
- [ ] Modo claro
- [ ] Converter em PWA

---

## 📬 Contacto

**👤 Autor:** [Jeysson Zerpa](https://www.linkedin.com/in/jeysson-leoncio-z-712661249/)
**📧 E-mail:** [jeyssonzerpa@gmail.com](mailto:jeyssonzerpa@gmail.com)
**📱 WhatsApp:** [+55 (35) 99888-9882](https://wa.me/5535998889882)
**🌍 Localização:** Prudentópolis — Paraná — Brasil

---

## 🪪 Licença

Projeto de uso pessoal e educacional. Podes reutilizar partes do código
**citando o autor**. O Three.js é distribuído sob licença MIT.

```
© 2025 Jeysson Zerpa — Todos os direitos reservados.
```

---

> "Transformo dados e automações em decisões inteligentes com propósito humano e impacto real."
>
> — Jeysson Zerpa
