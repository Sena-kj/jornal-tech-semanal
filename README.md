# 🗞️ Jornal Tech Semanal

Jornal automático sobre o mundo tech, com foco em **testes de IA** e um veredito de
**quais modelos usar agora e pra quê**. Gerado toda semana (domingo) por uma routine da
nuvem Anthropic, que lê a edição anterior e se auto-atualiza.

## Estrutura
- `fontes.md` — as 10 fontes (Top 10 verificada, peso em testes de IA)
- `PROMPT.md` — instrução da routine da nuvem (espelha o agente `jornalista-tech`)
- `recomendacoes-ia.md` — estado vivo de "quais IAs usar"
- `jornais/` — uma edição por domingo

## Como funciona
1. **Routine (domingo, nuvem):** clona este repo, lê `fontes.md` + última edição, coleta, escreve a nova edição, atualiza `recomendacoes-ia.md`, commita e dá push.
2. **Obsidian:** o plugin Obsidian Git puxa este repo → o jornal aparece no vault.
3. **Sob demanda:** na CLI, peça "gera o jornal agora" — o agente `jornalista-tech` faz na hora.

## Geração manual
```
@jornalista-tech gera a edição desta semana
```
