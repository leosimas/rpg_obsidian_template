# Instruções para agentes (Cursor / Copilot / outros)

Este documento descreve o uso do vault e como agentes de IA devem atuar nele.

## O que é este projeto

- **Obsidian Vault** para uma campanha de RPG (sistema definido pela campanha).
- Uso em **português (pt-BR)**.
- Objetivo: registrar e acessar informações da campanha para jogadores e mestre.
- Este vault é um **modelo**: mantenha a estrutura e as convenções ao criar conteúdo.

## Onde estão as regras

- **`README.md`** — estrutura de pastas, templates, convenções de nome e de frontmatter.
- **`AGENTS.md`** (este arquivo) — como o agente deve agir.

## Estrutura de pastas

| Pasta | Conteúdo |
|-------|----------|
| `0. Grupo` | sessões (`Sessões/`), fichas de PJ (`Personagens/`), regras da casa (`Regras da casa/`) |
| `1. Capítulos` | uma subpasta por capítulo, com nota principal e material de origem |
| `2. Lugares` | locais do cenário |
| `3. Personagens` | `importantes/` (NPCs centrais), `tabelas/` (opcionais), raiz (secundários) |
| `4. Itens` | `importantes/`, `tabelas/`, raiz (comuns) |
| `5. Organizações` | facções, guildas, cultos |
| `6. Monstros` | fichas de criaturas |
| `7. Templates` | modelos de nota |
| `z_imagens` | **todas** as imagens (subpastas por assunto) |

Não crie pastas ou arquivos fora dessa organização sem pedido explícito.

## Resumo do que o agente deve fazer

1. **Seguir a estrutura e os templates**
   - Antes de criar uma nota, leia o template correspondente em `7. Templates` e mantenha o frontmatter padronizado (`tipo`, `status`, `tags`, `atualizado`).

2. **Consultar o(s) capítulo(s) referenciado(s)**
   - Se o usuário citar um capítulo (ex.: “capítulo 1”), abrir a subpasta em `1. Capítulos` e ler o material (PDF, notas de cena) antes de responder ou criar conteúdo.

3. **Criar links de navegação**
   - Ao citar entidades, usar wiki-links: `[[Nome do Lugar]]`, `[[Nome do Personagem]]`, `[[Nome do Item]]`, `[[Nome da Organização]]`, `[[Nome do Monstro]]`, `[[Capítulo 01 - Título]]`.
   - Ruim: “Os PJs encontram o mercador Garvin na taverna.”
   - Bom: “Os PJs encontram o mercador [[Garvin]] na [[Taverna do Dragão]].”

4. **Usar a pasta geral de imagens**
   - Todas as imagens ficam em `z_imagens/<assunto>/`. Referenciar como `![[z_imagens/personagens/nome.png|300]]`.

5. **Notas de personagem**
   - `3. Personagens/importantes` para NPCs centrais; `3. Personagens/tabelas` para opcionais de tabela; raiz para secundários. PJs em `0. Grupo/Personagens`.
   - Uma nota por personagem, título = nome do arquivo = nome usado nos links.

6. **Notas de item**
   - `4. Itens/importantes` para itens de trama; `4. Itens/tabelas` para opcionais; raiz para comuns.

7. **Notas de sessão**
   - Em `0. Grupo/Sessões`, título `Sessão NN - AAAA-MM-DD - Título opcional`, com links para personagens, lugares e capítulos.

8. **Notas de lugar, organização, monstro e capítulo**
   - Lugares → `2. Lugares`; organizações → `5. Organizações`; monstros → `6. Monstros`; capítulos → subpasta em `1. Capítulos`.

9. **Frontmatter**
   - Manter os campos do template; não inventar valores. Atualizar `atualizado: AAAA-MM-DD` ao editar.

10. **Não inventar conteúdo de regras**
    - Ao registrar estatísticas, indicar a **fonte** (página/capítulo) e marcar como “ajustes da mesa” o que for adaptação própria.

## Atualizar instruções

- Edite este `AGENTS.md` para mudar a visão geral.
- Edite `README.md` para mudar estrutura, convenções ou templates.
- Para regras específicas de agentes com Cursor, crie `.cursor/rules/<nome>.mdc` com `alwaysApply: true`.
