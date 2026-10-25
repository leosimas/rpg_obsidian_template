---
tipo: hub
tags:
  - hub
atualizado: "{{date:YYYY-MM-DD}}"
---

# 🏠 Início

Ponto de entrada do vault. Troque o título acima pelo nome da campanha.

**Campanha:** [[Campanha]]
**Sistema:**
**Formato:** campanha longa | antologia | one-shots soltos | misto
**Mestre:**

---

## Agora na mesa

- **Aventura em jogo:** [[Capítulo 01 - Título]]
- **Grupo atual:** [[Grupo atual]]
- **Última sessão:** [[Sessão 01 - AAAA-MM-DD - Título opcional]]
- **Próxima sessão:** AAAA-MM-DD

## Atalhos

| Seção | Pasta | Para quê |
|-------|-------|----------|
| 🎲 Grupo | `0. Grupo` | grupo atual, PJs, sessões, regras da casa |
| 📖 Aventuras | `1. Capítulos` | one-shots, aventuras curtas e arcos |
| 🗺️ Lugares | `2. Lugares` | cidades, masmorras, regiões |
| 🧑 Personagens | `3. Personagens` | PNJs e criaturas com nome |
| 🎒 Itens | `4. Itens` | equipamentos, tesouros, artefatos |
| ⚔️ Organizações | `5. Organizações` | facções, guildas, cultos |
| 🐺 Monstros | `6. Monstros` | fichas de criaturas |
| 🧩 Templates | `7. Templates` | modelos de nota (Ctrl/Cmd+P → Inserir modelo) |
| 🖼️ Imagens | `z_imagens` | todas as ilustrações e mapas |

## Aventuras

| # | Aventura | Formato | Sessões | Nível |
|---|----------|---------|---------|-------|
| 01 | [[Capítulo 01 - Título]] | one-shot | 1 | 1 |

## Elenco de PJs

Pool completo em [[Personagens dos jogadores]]. Quem está em jogo agora: [[Grupo atual]].

- [[Nome do PJ 1]] — nível 1
- [[Nome do PJ 2]] — nível 1

## Rascunhos de one-shot

Ideias que ainda não viraram aventura: notas criadas com [[Template - One-shot]].

```query
tag:#one-shot
```

## Ganchos em aberto

- [ ] (promessa, ameaça ou mistério ainda não resolvido)
- [ ]

## Listas rápidas

### Aventuras
```query
path:"1. Capítulos" -path:"7. Templates"
```

### Personagens importantes
```query
path:"3. Personagens/importantes"
```

### Monstros
```query
path:"6. Monstros" -path:"7. Templates"
```

### Sessões
```query
path:"0. Grupo/Sessões" -path:"7. Templates"
```
