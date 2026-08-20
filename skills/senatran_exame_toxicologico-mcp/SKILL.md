---
name: senatran_exame_toxicologico-mcp
description: Skill da REST API do SENATRAN: Consultar Exame Toxicológico na MCP.AI: 1 endpoint em /api/senatran_exame_toxicologico. SENATRAN: Consultar Exame Toxicológico, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SENATRAN: Consultar Exame Toxicológico — REST API skill

Você tem acesso à **SENATRAN: Consultar Exame Toxicológico** REST API na MCP.AI.

> SENATRAN: Consultar Exame Toxicológico, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/senatran_exame_toxicologico
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/senatran_exame_toxicologico/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cpf":"...","birthdate":"...","data_vencimento_cnh":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/senatran_exame_toxicologico/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `senatran_exame_toxicologico_consultar`

SENATRAN: Consultar Exame Toxicológico, consulta em fonte oficial. _(POST /api/senatran_exame_toxicologico/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Sim | Parâmetro de consulta "cpf". |
| `birthdate` | string | Sim | Parâmetro de consulta "birthdate". |
| `data_vencimento_cnh` | string | Sim | Parâmetro de consulta "data_vencimento_cnh". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_senatran_exame_toxicologico` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
