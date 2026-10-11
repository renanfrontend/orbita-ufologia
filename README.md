# Órbita — Observatório de Ufologia

[![Deploy to GitHub Pages](https://github.com/renanfrontend/orbita-ufologia/actions/workflows/deploy.yml/badge.svg)](https://github.com/renanfrontend/orbita-ufologia/actions/workflows/deploy.yml)

> © 2026 Renan Augusto dos Santos. **Todos os direitos reservados.** Código destinado a portfólio e avaliação profissional: copiar, adaptar ou reutilizar exige autorização por escrito. Veja [Licença e direitos autorais](#licença-e-direitos-autorais).

Um app de ufologia em português para explorar casos históricos, consultar fontes e registrar observações do céu. O **Órbita** reúne dois interesses pessoais de Renan Augusto dos Santos: **tecnologia e ufologia**, com uma experiência que incentiva a curiosidade, a investigação e o pensamento crítico.

A proposta é olhar para o desconhecido com contexto: distinguir relatos, registros e interpretações. **Um fenômeno não identificado não é, por si só, evidência de origem extraterrestre.**

## O que dá para fazer

- **Explorar seis casos históricos:** Operação Prato, Encontro do Nimitz, Incidente de Roswell, Noite Oficial dos OVNIs, Luzes de Phoenix e Projeto Blue Book.
- **Consultar os detalhes dos casos**, com contexto, limites das evidências e links para fontes.
- **Buscar por caso, lugar ou ano**, com suporte a buscas sem acentos.
- **Filtrar por Brasil, casos internacionais e favoritos.**
- **Salvar casos favoritos** no próprio navegador.
- **Aprender a observar:** registrar contexto, comparar explicações comuns, preservar arquivos originais e separar fatos de interpretações.
- **Manter um diário pessoal** com título, data, horário, local, fuso e descrição da observação.
- **Excluir registros e exportar o diário em JSON**, para guardar uma cópia.
- Navegar em uma interface responsiva, com identidade visual de observatório, tons escuros e verde-lima.

## Stack

HTML5 · CSS3 · JavaScript · SVG · Web Storage API (`localStorage`).

Aplicação estática, sem frameworks, compilação ou dependências de execução instaladas. As fontes **DM Sans** e **Space Grotesk** são carregadas pelo Google Fonts; fontes de sistema são usadas quando o serviço não está disponível.

## Arquitetura

```text
dist/
├── index.html       # estrutura, navegação, modais e formulários
├── style.css        # identidade visual e layout responsivo
└── app.js           # catálogo, busca, favoritos, diário e exportação
README.md            # documentação do projeto
.github/workflows/
└── deploy.yml       # publicação automática no GitHub Pages
LICENSE              # termos de direitos reservados
.gitignore           # exclusões de arquivos locais
```

### Como os dados são armazenados

Os casos e os links de referência estão no código do app. Favoritos e observações ficam no `localStorage`, nas chaves `orbita-favorites` e `orbita-entries`.

Não há servidor de registros, conta de usuário ou sincronização entre dispositivos. **As observações não são enviadas a uma comunidade ou serviço remoto.** O carregamento de fontes e a abertura dos links externos dependem dos respectivos serviços.

Limpar os dados do navegador, usar outro navegador ou mudar a origem do site pode tornar os registros indisponíveis. Use **Exportar registros** para manter uma cópia. A versão atual exporta o diário, mas não importa arquivos JSON.

## Rodando localmente

Clone o repositório e sirva a pasta `dist/` com um servidor HTTP estático. Com Python 3 instalado:

```bash
git clone https://github.com/renanfrontend/orbita-ufologia.git
cd orbita-ufologia
python3 -m http.server 8080 --directory dist
```

Abra `http://localhost:8080` no navegador. Não é necessário executar `npm install` ou fazer build.

## Publicação

A pasta `dist/` pode ser hospedada em qualquer serviço de sites estáticos. Ela já contém os arquivos necessários para servir o app.

A configuração de publicação está em `.github/workflows/deploy.yml`. Depois de habilitar **Settings → Pages → Build and deployment → Source: GitHub Actions**, cada push na `main` publica a pasta `dist/`. Também é possível iniciar o fluxo manualmente em **Actions → Deploy to GitHub Pages → Run workflow**.

URL prevista após a primeira publicação bem-sucedida: `https://renanfrontend.github.io/orbita-ufologia/`. Essa URL só estará ativa após o deploy ser concluído.

## Fontes e contexto

- [Arquivo Nacional](https://www.gov.br/arquivonacional/pt-br): ponto de partida para pesquisar a documentação brasileira sobre OVNIs.
- [AARO — imagens oficiais de UAP](https://www.aaro.mil/UAP-Cases/Official-UAP-Imagery/): contexto para registros militares divulgados oficialmente.
- [Força Aérea dos EUA — The Roswell Report](https://www.af.mil/The-Roswell-Report/): explicação oficial para o incidente de Roswell.
- [National Archives — Project Blue Book](https://www.archives.gov/research/military/air-force/ufos): documentação do programa americano.
- [NASA — UAP](https://science.nasa.gov/uap/): estudo de fenômenos anômalos não identificados.
- [Britannica — unidentified flying object](https://www.britannica.com/topic/unidentified-flying-object): contexto geral sobre OVNIs.

O catálogo é uma seleção educativa, não um banco de dados em tempo real. Alguns links apontam para portais de pesquisa, e não para documentos individuais. As cenas dos cartões e a esfera orbital são **ilustrações artísticas em SVG**, não fotografias ou registros dos fenômenos.

## Autoria

Concepção do projeto e direção temática por **Renan Augusto dos Santos** ([renanaugusto.com.br](https://renanaugusto.com.br) · [contato@renanaugusto.com.br](mailto:contato@renanaugusto.com.br)), da Up Technology Innovations. Implementação inicial desenvolvida com apoio de inteligência artificial (Codex).

O Órbita nasce do interesse pessoal por ufologia, além da tecnologia, e transforma essa curiosidade em uma ferramenta de exploração e registro.

## Licença e direitos autorais

© 2026 Renan Augusto dos Santos. **Todos os direitos reservados.**

Este não é um projeto open source. A disponibilização do código para portfólio e avaliação profissional não concede autorização de uso. Sem autorização por escrito, não é permitido:

- copiar, modificar, redistribuir ou usar comercialmente o projeto, no todo ou em parte;
- reescrever o projeto em outra stack a partir deste repositório, ou reutilizar a identidade visual Órbita, a interface e os textos autorais;
- apresentar o projeto, ou parte dele, como trabalho próprio em portfólios, processos seletivos ou propostas comerciais;
- usar o conteúdo autoral do repositório para treinar, ajustar ou avaliar modelos de IA.

Os termos completos estão em [LICENSE](LICENSE). Fontes e materiais de terceiros mantêm suas próprias licenças e direitos. Pedidos de autorização: [contato@renanaugusto.com.br](mailto:contato@renanaugusto.com.br).

---

## 🇺🇸 English

**Órbita** is a Portuguese-language ufology app by **Renan Augusto dos Santos**, bringing together his personal interests in technology and ufology. Explore six historical cases, consult sources, filter and bookmark cases, learn observation methods, and keep a personal observation journal with JSON export. Built with HTML, CSS, JavaScript and SVG. Bookmarks and observations stay in the browser's local storage; there is no account, server-side journal or device synchronization.

The app distinguishes reports, documented records and interpretations. An unidentified phenomenon does not establish an extraterrestrial origin. All landscape and orbital visuals are artistic illustrations.

© 2026 Renan Augusto dos Santos. **All rights reserved.** This is not open source. Copying, modifying, porting, redistributing, commercial use, presenting it as your own work or using original project content to train AI models requires written permission. See [LICENSE](LICENSE). Contact: [contato@renanaugusto.com.br](mailto:contato@renanaugusto.com.br) · [renanaugusto.com.br](https://renanaugusto.com.br).
