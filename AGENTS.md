# ZAPHYX LABS — AGENTS.md

## 1. Visão do produto

A Zaphyx Labs é um laboratório criativo de soluções digitais.

Desenvolve sites, landing pages e automações para pequenos
e médios negócios.

O projeto possui duas experiências:

1. Website institucional com identidade visual própria.
2. Lab de Serviços para geração de mockups comerciais.

Assinatura da marca:
"Ideias em órbita. Negócios em movimento."

## 2. Direção visual

Identidade oficial: Ideias em Órbita.

A estética deve transmitir:
- Sofisticação e profissionalismo.
- Exploração e descoberta.
- Criatividade e inteligência.
- Tecnologia e movimento.
- Atmosfera espacial sutil.

Evitar:
- Estética infantil ou excessivamente gamer.
- Cyberpunk exagerado.
- Elementos decorativos sem propósito.
- Layouts genéricos de agências de tecnologia.
- Referências explícitas a obras de ficção.

### Paleta

Background: #0B1020
Text:       #F4F6FA
Primary:    #58DDE0
Accent:     #F4B860

## 3. Hero 3D

O elemento central será um símbolo Z tridimensional,
com acabamento metálico e módulos orbitais.

Os módulos representam:
- Sites.
- Landing pages.
- Automações.

Tecnologias:
- Three.js.
- React Three Fiber.

Requisitos:
- Renderização otimizada.
- Responsividade.
- Animações discretas.
- Acessibilidade.
- Respeito a prefers-reduced-motion.
- Alternativa estática quando necessário.

## 4. Arquitetura

Estrutura planejada:

apps/
  web/    React + TypeScript + Vite
  api/    NestJS (implementação futura)

docs/
  architecture/
  briefings/

O projeto deve priorizar modularidade,
separação de responsabilidades e simplicidade.

Não criar módulos futuros antecipadamente.

## 5. Lab de Serviços

O visitante informa:
- Nome.
- Telefone ou WhatsApp.
- E-mail.
- Nome da empresa.
- Segmento.
- Descrição do negócio.
- Preferências de cores.

O Lab gera uma imagem PNG conceitual mostrando
como poderia ser o site do negócio.

O Lab não gera um site funcional no MVP.

A imagem exibida ao visitante deverá ser a mesma
armazenada para consulta comercial posterior.

## 6. CRM

O projeto utilizará a base:

Zaphyx Labs | CRM — Leads

Integração futura com a API do Notion.

Requisitos:
- Registro do lead.
- Identificador único da simulação.
- Referência persistente à imagem.
- Histórico de interesse comercial.
- Tratamento de erros.
- Prevenção de duplicidades.

Credenciais nunca devem ser expostas no frontend.

Aplicar princípios da LGPD, incluindo transparência,
finalidade definida e proteção dos dados pessoais.

## 7. Padrões de desenvolvimento

- TypeScript em modo estrito.
- Componentes com responsabilidade definida.
- Código simples, legível e reutilizável.
- Evitar abstrações prematuras.
- Validação de entradas.
- Tratamento explícito de erros.
- Sem dependências desnecessárias.
- Sem credenciais no repositório.
- Acessibilidade e responsividade.
- Testes orientados a comportamentos relevantes.

## 8. Fluxo de trabalho obrigatório

O desenvolvimento ocorrerá em fatias.

Antes de implementar:
1. Analisar o código existente.
2. Apresentar diagnóstico.
3. Informar arquivos afetados.
4. Justificar decisões técnicas.
5. Definir critérios de aceitação.
6. Aguardar aprovação.

Após implementar:
1. Executar lint.
2. Executar build.
3. Executar testes aplicáveis.
4. Informar resultados.
5. Resumir alterações.
6. Aguardar revisão antes do commit.

Não implementar funcionalidades fora da fatia aprovada.

## 9. Fatia atual

Fatia 1.2.1 — Design System.

Escopo:
- Configuração do Tailwind CSS 4.
- Tokens visuais.
- Tipografia.
- Estilos globais.
- Fundação de acessibilidade.

Não implementar nesta etapa:
- Hero completo.
- Cena 3D.
- Lab de Serviços.
- Backend.
- Integração com Notion.

O Codex deve apresentar um plano antes de modificar arquivos.
