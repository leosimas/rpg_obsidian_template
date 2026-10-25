# Instruções para agentes (Cursor / Copilot / outros)

Este documento descreve o uso do vault e como agentes de IA devem atuar nele.

## O que é este projeto

- **Obsidian Vault** para uma campanha de RPG (sistema definido pela campanha).
- Uso em **português (pt-BR)**.
- Aceita **campanha longa**, **antologia de one-shots** ou mistura das duas; o grupo de PJs pode mudar entre aventuras e os PJs podem subir de nível.
- Este vault é um **modelo**: mantenha a estrutura e as convenções ao criar conteúdo.

## Onde estão as regras

- **`README.md`** — estrutura, templates, convenções de nome, frontmatter e cenários de uso.
- **`AGENTS.md`** (este arquivo) — como o agente deve agir.

## Estrutura de pastas

| Pasta | Conteúdo |
|-------|----------|
| `0. Grupo` | `Campanha.md`, `Grupo atual.md`, `Sessões/`, `Personagens/` (pool de PJs), `Regras da casa/`, `One-shots/` (rascunhos) |
| `1. Capítulos` | uma subpasta por aventura, com nota principal e material de origem |
| `2. Lugares` | locais do cenário |
| `3. Personagens` | `importantes/`, `tabelas/`, raiz |
| `4. Itens` | `importantes/`, `tabelas/`, raiz |
| `5. Organizações` | facções, guildas, cultos |
| `6. Monstros` | fichas de criaturas |
| `7. Templates` | modelos de nota |
| `z_imagens` | **todas** as imagens (subpastas por assunto) |

Não crie pastas ou arquivos fora dessa organização sem pedido explícito.

## Conceitos que o agente precisa respeitar

1. **Campanha ≠ aventura ≠ grupo ≠ sessão.**
   - `Campanha.md` guarda formato, progressão e regras de troca de grupo.
   - `Grupo atual.md` é quem joga **agora**; pode ser reescrito a cada aventura.
   - O **pool de PJs** em `0. Grupo/Personagens` inclui ativos, de reserva e aposentados — nunca apague uma ficha de PJ; mude `status`.
2. **Formato da aventura** (`formato: one-shot | aventura curta | arco longo`) muda a profundidade da nota, não a estrutura.
3. **Progressão** é registrada em dois lugares: na aventura (`nivel_pjs` → `nivel_final`) e na ficha do PJ (tabela **Progressão**). O bloco de estatísticas da ficha é sempre o nível atual.
4. **One-shot:** a nota da sessão única preenche também **Fechamento de aventura**.
5. **PJs de one-shot** usam `Template - PJ One-shot` com `status: one-shot`; só viram PJ recorrente se o jogador quiser (mudar `status: ativo`, `tipo_elenco: rotativo`).

## Resumo do que o agente deve fazer

1. **Seguir a estrutura e os templates**
   - Antes de criar uma nota, leia o template correspondente em `7. Templates` e mantenha o frontmatter padronizado.

2. **Consultar o material da aventura**
   - Se o usuário citar uma aventura/capítulo, abrir a subpasta em `1. Capítulos` e ler PDF/notas antes de responder ou criar conteúdo.

3. **Criar links de navegação**
   - `[[Nome do Lugar]]`, `[[Nome do Personagem]]`, `[[Nome do Item]]`, `[[Nome da Organização]]`, `[[Nome do Monstro]]`, `[[Capítulo 01 - Título]]`, `[[Grupo atual]]`.
   - Ruim: “Os PJs encontram o mercador Garvin na taverna.”
   - Bom: “Os PJs encontram o mercador [[Garvin]] na [[Taverna do Dragão]].”

4. **Usar a pasta geral de imagens**
   - Todas as imagens em `z_imagens/<assunto>/`, referenciadas como `![[z_imagens/personagens/nome.png|300]]`.

5. **Notas de personagem (NPC)**
   - `3. Personagens/importantes`, `tabelas/` ou raiz conforme o papel. Uma nota por personagem.

6. **Notas de item**
   - `4. Itens/importantes`, `tabelas/` ou raiz conforme o papel.

7. **Notas de sessão**
   - Em `0. Grupo/Sessões`, título `Sessão NN - AAAA-MM-DD - Título opcional`, sempre com link para a aventura e para o grupo.

8. **Lugar, organização, monstro**
   - `2. Lugares`, `5. Organizações`, `6. Monstros`.

9. **Ao fechar uma aventura**
   - Preencher o **Fechamento de aventura** na sessão final; atualizar `status` da aventura, a tabela **Progressão** dos PJs, o `Grupo atual` (com histórico) e o estado do mundo em `Campanha.md`.

10. **Não inventar conteúdo de regras**
    - Ao registrar estatísticas, indicar a **fonte** (página/capítulo) e marcar como “ajustes da mesa” o que for adaptação própria.

## Atualizar instruções

- Edite este `AGENTS.md` para mudar a visão geral.
- Edite `README.md` para mudar estrutura, convenções ou templates.
- Para regras específicas de agentes com Cursor, crie `.cursor/rules/<nome>.mdc` com `alwaysApply: true`.
