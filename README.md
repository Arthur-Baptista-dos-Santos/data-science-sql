# `data-science-sql: Scripts SQL e Analise de Dados`

> Portfolio de Data Science: schema relacional Oracle SQL (DDL), scripts DML/DQL com 200+ insercoes e consultas analiticas, e analise HTML interativa de dados de seguros. Sprints 2 a 4, FIAP 2025.

---

## `Tecnologias`

![SQL](https://img.shields.io/badge/SQL-Oracle%20%2F%20ANSI-blue)
![HTML](https://img.shields.io/badge/HTML-analise%20interativa-orange)
![License](https://img.shields.io/badge/license-MIT-green)

---

## `Arquivos`

| Arquivo | Sprint | Descricao |
|---------|--------|---------|
| `analise_sprint2.html` | Sprint 2 · 2025-1 | Analise de dados interativa em HTML com graficos e tabelas |
| `schema_sprint3.sql` | Sprint 3 · 2025-2 | DDL: schema relacional completo (tabelas, constraints, sequences) |
| `dml_dql_sprint4.sql` | Sprint 4 · 2025-2 | DML: 200+ insercoes + DQL: consultas analiticas |

---

## `Schema relacional (sprint3)`

```sql
-- Tabelas principais
T_AICSS_PRODUTO       produto sinistrado
T_AICSS_CLIENTE       dados do segurado
T_AICSS_SEGURO        apolice vinculada ao cliente
T_AICSS_SINISTRO      ocorrencia vinculada a apolice
T_AICSS_ENDERECO      localizacao do produto/cliente
T_AICSS_VEICULO       dados do veiculo (se seguro auto)

-- Constraints
PRIMARY KEY, FOREIGN KEY, NOT NULL, CHECK (valor > 0)
SEQUENCE para auto-incremento de IDs
```

---

## `Consultas DQL (sprint4)`

```sql
-- Exemplos de consultas implementadas
SELECT tipo_seguro, COUNT(*), SUM(valor_premio)
FROM sinistros
GROUP BY tipo_seguro HAVING COUNT(*) > 5;

SELECT nome, SUM(s.valor_indenizacao) AS total
FROM clientes c JOIN sinistros s ON c.id = s.cliente_id
GROUP BY nome ORDER BY total DESC;
```

---

## `Analise HTML (sprint2)`

Dashboard estatico com:
- Distribuicao de sinistros por tipo e regiao
- Evolucao mensal de premios
- Top 10 produtos mais sinistrados
- Mapa de calor de correlacoes

---

## `Como usar`

```sql
-- No Oracle SQL Developer ou DBeaver:
-- 1. Execute schema_sprint3.sql (DDL)
-- 2. Execute dml_dql_sprint4.sql (insercoes + consultas)

-- Para analise HTML:
-- Abra analise_sprint2.html no navegador
```

---

## `Licenca`

Distribuido sob a licenca MIT.

---

## `Autor`

**Arthur Baptista dos Santos**
RM 565346 · Inteligencia Artificial · FIAP 2025-2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Arthur%20Baptista-0077B5?logo=linkedin)](https://linkedin.com/in/arthur-baptista-dos-santos)
[![GitHub](https://img.shields.io/badge/GitHub-Arthur--Baptista--dos--Santos-181717?logo=github)](https://github.com/Arthur-Baptista-dos-santos)
