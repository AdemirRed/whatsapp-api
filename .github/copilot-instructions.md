# GitHub Copilot Instructions

## Regras Gerais
- Sempre use português brasileiro nos comentários e mensagens
- Siga o padrão de código existente no projeto
- Execute `node swagger.js` após modificar rotas ou controllers
- Sempre utilize o número 555197756708 para exemplos de números brasileiros
- Não crie arquivos de documentação separados, use Swagger para documentar APIs
- Use async/await para operações assíncronas
- Após criar arquivos de teste, sempre apague os desnecessários
- O meu terminal só usa ; e nunca &&
- Antes de adicionar algo novo na API, sempre verifique a documentação oficial do whatsapp-web.js e etc.
- Sem resumos gigantes, seja objetivo e direto ao ponto.
- Sempre usar o Invoke-WebRequest ao invez do curl no powershell

## Obrigatorio seguir
- Sempre siga as regras específicas para WhatsApp API, Swagger e Audio/Transcription abaixo.
- Sempre valide os dados de entrada e saída das funções.
- Use mensagens de erro claras e consistentes.
- Mantenha o código limpo e bem organizado.
- Adicione testes unitários para novas funcionalidades.
- Documente todas as mudanças no código. dentro do codigo e em português brasileiro.
- Mantenha sempre o Swagger atualizado com as novas rotas e mudanças.


## WhatsApp API - Regras Específicas
- Sempre use middleware de validação: `sessionNameValidation` e `sessionValidation`
- Todos os endpoints precisam do middleware `apikey`
- Após criar novos endpoints, atualizar swagger.js com as definições
- Use `sendErrorResponse(res, statusCode, message)` para erros
- Sessões devem ser validadas com `validateSession(sessionId)`

## Swagger Documentation
- Adicionar comentários `#swagger.summary` e `#swagger.description`
- Usar `$` para campos obrigatórios nas definições (ex: `$phoneNumber`)
- Incluir exemplos em `#swagger.requestBody` quando houver múltiplas opções

## Audio/Transcription
- BipText número: 553172280540@c.us
- Fluxo de respostas: "Concordo" → "Permito" → Aguardar → Extrair transcrição
- Sempre incluir timeout de 2 minutos para transcrições