---
tipo: hub
tags:
  - hub
atualizado: "{{date:YYYY-MM-DD}}"
---

# 🏠 Início

Ponto de entrada do vault. Troque o título acima pelo nome da campanha e preencha a linha de baixo.

**Campanha:**
**Sistema:**
**Mestre:**
**Status:** planejamento | em andamento | concluída

---

## Atalhos

| Seção | Pasta | Para quê |
|-------|-------|----------|
| 🎲 Grupo | `0. Grupo` | sessões, PJs, regras da casa |
| 📖 Capítulos | `1. Capítulos` | arcos e aventuras, com o material de origem |
| 🗺️ Lugares | `2. Lugares` | cidades, masmorras, regiões |
| 🧑 Personagens | `3. Personagens` | PNJs, PJs e criaturas com nome |
| 🎒 Itens | `4. Itens` | equipamentos, tesouros, artefatos |
| ⚔️ Organizações | `5. Organizações` | facções, guildas, cultos |
| 🐺 Monstros | `6. Monstros` | fichas de criaturas |
| 🧩 Templates | `7. Templates` | modelos de nota (Ctrl/Cmd+P → Inserir modelo) |
| 🖼️ Imagens | `z_imagens` | todas as ilustrações e mapas |

## Estado da campanha

- **Capítulo atual:** [[Capítulo 01 - Título]]
- **Última sessão:** [[Sessão 01 - AAAA-MM-DD - Título opcional]]
- **Próxima sessão:** AAAA-MM-DD

## Grupo

- [[Nome do PJ 1]]
- [[Nome do PJ 2]]

## Linha do tempo da campanha

| Data in-game | Evento | Sessão | Capítulo |
|--------------|--------|--------|----------|
|  |  | [[Sessão 01 - AAAA-MM-DD - Título opcional]] | [[Capítulo 01 - Título]] |

## Ganchos em aberto

- [ ] (promessa, ameaça ou mistério ainda não resolvido)
- [ ]

## Listas rápidas

### Todos os lugares
```query
path:"2. Lugares" -path:"7. Templates"
```

### Todos os personagens importantes
```query
path:"3. Personagens/importantes"
```

### Todos os monstros
```query
path:"6. Monstros" -path:"7. Templates"
```

### Últimas sessões
```query
path:"0. Grupo/Sessões" sort:modified
```
