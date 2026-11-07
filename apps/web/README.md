# Zaphyx Labs — Web

Fundação visual da identidade **Ideias em órbita**, em React, TypeScript,
Vite e Tailwind CSS 4. A tela atual apresenta somente a marca e sua assinatura.

## Desenvolvimento e validação

Execute os comandos dentro de `apps/web`:

```sh
npm ci
npm run dev
npm run lint
npm run build
npm run preview
```

Na raiz do repositório, execute `git diff --check` para verificar o diff.
O build inclui a verificação do TypeScript em modo estrito.
Não há suíte de testes automatizados configurada nesta fatia.

## Organização dos estilos

- `src/index.css`: entrada única; importa Tailwind, tokens e estilos base.
- `src/styles/tokens.css`: tema centralizado em `@theme`, compartilhado por
  utilitários Tailwind e variáveis CSS. As cores padrão do Tailwind são
  substituídas pela paleta da marca.
- `src/styles/base.css`: estilos globais em `@layer base`, hierarquia de títulos,
  links, foco, seleção e preferência de movimento reduzido.

### Tokens e uso

| Grupo | Tokens / utilitários |
| --- | --- |
| Paleta oficial | `background` (#0B1020), `foreground` (#F4F6FA), `primary` (#58DDE0), `accent` (#F4B860) |
| Cores derivadas | `surface`: 5% do texto sobre o fundo; `muted`: 70%; `border`: 20% |
| Tipografia | `font-sans` e `font-heading`, independentes para futura fonte de marca |
| Escala textual | `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-display` |
| Espaçamento | Unidade de 0.25rem; priorizar 1, 2, 3, 4, 6, 8, 12 e 16 unidades |
| Largura | `max-w-content` (72rem), `max-w-reading` (65ch) |
| Raios | `rounded-sm` (0.25rem), `rounded-md` (0.5rem) |

Exemplos: `bg-background text-foreground`, `text-primary`, `text-muted`,
`px-6 sm:px-8`. Não duplicar valores oficiais nos componentes.
A cor `border` serve a separadores decorativos; não garante contraste para
limites de controles. Usar contraste medido para qualquer interação futura.

## Acessibilidade e responsividade

- Tema escuro fixo, fontes do sistema, medidas relativas e texto fluido.
- Foco visível em ciano e links sublinhados.
- Seleção com texto escuro sobre ciano.
- Respeito a `prefers-reduced-motion`; nenhuma animação foi introduzida.
- Validar no navegador em 320, 768 e 1440 px, com zoom de 200%, teclado,
  preferência por tema claro e redução de movimento.
- Medir contraste: pelo menos 4.5:1 para texto comum e 3:1 para texto grande
  e indicadores visuais de interação. Usar fundo escuro como texto sobre
  preenchimentos ciano ou âmbar, verificando cada combinação.

## Referência e escopo

Referência oficial: `public/references/zaphyx-ideias-em-orbita.png`.
A imagem é material de consulta, não é renderizada nem substituída pela aplicação.
Esta fatia não implementa Header definitivo, Hero, objetos 3D, Lab, formulários,
backend ou integrações. Não foram adicionadas dependências.
