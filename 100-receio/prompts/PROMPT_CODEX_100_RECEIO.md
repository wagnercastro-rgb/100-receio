Prompt para o Codex — finalizar e revisar o 100 Receio
Você está trabalhando no repositório do 100 Receio. Leia primeiro README.md, docs/design_system.md, supabase/schema.sql e inspecione todos os arquivos existentes.

O projeto usa HTML semântico, CSS e JavaScript Vanilla com módulos ES, Supabase JS Client, SweetAlert2 e Lucide Icons. Não introduza React, Vue, Angular, TypeScript, jQuery ou ferramentas de build adicionais.
Objetivo
Revisar, completar, corrigir e testar o site de receitas. Não recrie tudo do zero se já houver uma implementação funcional. Preserve decisões compatíveis e não apague trabalho existente sem justificativa.
Requisitos funcionais
1. Página inicial com busca e receitas públicas.
2. Cadastro, login, logout e recuperação de senha via Supabase Auth.
3. Área privada com receitas do usuário.
4. Criar e editar receitas com título, descrição, categoria, tempo, rendimento, imagem por URL, visibilidade, observações, ingredientes e etapas.
5. Exibir detalhes de receitas públicas e privadas conforme RLS.
6. Excluir receitas com confirmação.
7. Favoritar e desfavoritar receitas públicas de outros usuários.
8. Compartilhar URL de receitas públicas; nunca expor receitas privadas.
9. Estados de carregamento, erro, vazio e sucesso em português.
10. Layout responsivo e acessível, seguindo o design system.
Fontes de verdade e banco
Use supabase/schema.sql como referência para nomes reais de tabelas, colunas, relacionamentos e políticas. Não invente colunas. Não desative nem contorne RLS. A chave service_role nunca pode aparecer no frontend.

As tabelas esperadas neste SQL são categorias_receitas, receitas, ingredientes_receita, etapas_receita e receitas_favoritas. Confirme seus campos no arquivo antes de escrever consultas.

O SQL permite leitura anônima apenas de receitas públicas e seus ingredientes/etapas; operações de escrita e favoritos exigem autenticação. Respeite essa distinção.
Configuração
A configuração local usa .env e server.js. O navegador recebe js/config.js gerado/servido com SUPABASE_URL e SUPABASE_ANON_KEY. Não tente ler .env diretamente no browser. Mantenha .env e js/config.js fora do Git.
Revisão de qualidade
- Verifique imports e caminhos de todos os módulos.
- Verifique formulários, validação, filtros e operações Supabase.
- Garanta que usuários não possam editar ou excluir receitas de terceiros.
- Garanta que visitantes não autenticados só vejam receitas públicas.
- Verifique se ingredientes e etapas aparecem na ordem correta.
- Verifique comportamento sem imagem e sem receitas cadastradas.
- Execute os testes que forem possíveis e informe claramente o que não pôde ser testado por falta de credenciais ou projeto Supabase.
- Não declare testes como aprovados sem executá-los.
Entrega
Faça as alterações diretamente no repositório. Ao terminar, liste arquivos criados/alterados, funcionalidades concluídas, testes executados, configurações manuais restantes e limitações conhecidas. Não substitua o projeto por um mockup.
