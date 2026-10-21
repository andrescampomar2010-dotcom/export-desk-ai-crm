# Export Desk · Agente IA + CRM (prototipo)

**ES** · Prototipo de un agente comercial con IA para una pyme exportadora. Un widget de chat cualifica al visitante en su idioma, crea la ficha en un CRM kanban, genera el borrador de oferta desde la tarifa (los precios nunca salen sin revisión humana), programa el seguimiento D+3 / D+7 / D+14 y capta peticiones desde el correo. Incluye gemelo digital (conocimiento + stock + capacidad → plazos orientativos), memoria de clientes y conectores MCP opcionales (CRM, buzón y base de conocimiento). La empresa de la demo es 100 % ficticia: «ACME Ventilación Industrial», un fabricante español de equipos de ventilación industrial que exporta a Europa (dominios `.test`, personas y precios inventados).

**EN** · Prototype of an AI sales agent for an exporting SME. A chat widget qualifies visitors in their own language, creates the record in a kanban CRM, drafts quotes from the price list (prices never go out without human review), schedules D+3 / D+7 / D+14 follow-ups and captures requests from the mailbox. Includes a digital twin (knowledge + stock + capacity → indicative lead times), customer memory and optional MCP connectors (CRM, mailbox and knowledge base). The demo company is 100% fictitious: "ACME Ventilación Industrial", a Spanish manufacturer of industrial ventilation equipment exporting across Europe (`.test` domains, invented people and prices).

## Qué hace / What it does

- Agente web ES/FR/EN en modo guion (sin conexión) y en cualquier idioma con una clave de API de Anthropic; escenarios de demo que se reproducen solos. · ES/FR/EN scripted mode offline, any language with an Anthropic API key; self-playing demo scenarios.
- Pipeline CRM kanban con asignación por país/idioma, scoring explicable y consentimiento RGPD (sin consentimiento, los datos de contacto se descartan). · Kanban pipeline with country/language routing, explainable scoring and GDPR consent handling.
- Ofertas ES/FR/EN desde tarifa con nota fiscal del destino (intracomunitaria, Reino Unido, Canarias, exportación), PDF imprimible y aprobación humana obligatoria. · Trilingual quotes with destination tax notes, printable PDF, mandatory human approval.
- Captación desde email (pegado o buzón vía MCP): extracción con IA o por reglas locales, y detección de respuestas a ofertas por número. · Email capture (pasted or mailbox via MCP) with AI or local-rule extraction; detects quote replies.
- Gemelo digital: base de conocimiento consultable, stock y capacidad de fabricación que alimentan plazos orientativos, y simulador «¿qué pasa si…?». · Digital twin: searchable knowledge base, stock and manufacturing capacity feeding indicative lead times, plus a what-if simulator.
- Memoria del agente: reconoce al cliente que vuelve, mantiene al mismo comercial y nunca revela datos anteriores al visitante. · Agent memory: recognizes returning customers, keeps the same sales rep, never leaks past data to the visitor.
- Eventos JSON a webhook (n8n / Make / Zapier) y conectores MCP opcionales para CRM, correo y conocimiento. · JSON events to webhooks (n8n / Make / Zapier) and optional MCP connectors for CRM, mail and knowledge.
- Un único archivo HTML, sin build; persistencia en localStorage. · Single HTML file, no build; persists in localStorage.

## Cómo probarlo / Run it

Demo en vivo / Live demo: **https://andrescampomar2010-dotcom.github.io/export-desk-ai-crm/** — o abre `index.html` en un navegador. Funciona sin clave API (modo guion); con una clave de Anthropic en «Config» usa IA en tiempo real. / Or open `index.html` in a browser. Works offline in scripted mode; add an Anthropic API key in "Config" for live AI.

## Stack

HTML + CSS + JavaScript en un solo archivo, sin frameworks · API de Anthropic (opcional) · MCP (Model Context Protocol) · webhooks n8n/Make.

## Datos / Data

Toda empresa, persona, precio y email es ficticio («ACME», dominios `.test`); cualquier parecido con empresas reales es pura coincidencia. · Every company, person, price and email is fictitious ("ACME", `.test` domains); any resemblance to real companies is pure coincidence.

## Licencia / License

MIT
