# Hermes Study Agent

Um projeto de assistente pessoal de estudos utilizando Hermes Agent, DeepSeek API, Docker, Linux e Telegram.

## Objetivo

Construir um assistente pessoal acessível pelo Telegram para ajudar a planejar a rotina de estudos, registrar sessões, acompanhar o desempenho e identificar dificuldades ao longo da preparação para o ENEM e o vestibular da UFU.

## Tecnologias

- **Linux:** Debian 13.7 em VPS
- **Docker:** execução do agente em contêiner
- **Hermes Agent:** agente de IA e gateway de comunicação
- **DeepSeek API:** modelo de linguagem utilizado
- **Telegram Bot API:** interface de conversa

## Arquitetura

O usuário envia uma mensagem pelo Telegram. O gateway do Hermes recebe a mensagem, encaminha o processamento ao modelo de IA configurado e devolve a resposta ao usuário.

A VPS mantém o serviço em execução, enquanto o Docker facilita a inicialização e a persistência dos dados do agente.

## Implementação atual

- [x] Contratação e preparação da VPS
- [x] Configuração do acesso SSH
- [x] Instalação do Docker
- [x] Inicialização do Hermes Agent
- [x] Configuração do provider DeepSeek
- [x] Conexão do gateway ao Telegram
- [ ] Transferência das skills personalizadas para a VPS
- [ ] Registro automatizado de sessões de estudo
- [ ] Análise de aproveitamento e dificuldades
- [ ] Planejamento de estudos integrado ao histórico
- [ ] Integrações adicionais, conforme necessidade

## Aprendizados

Durante a implantação, foram explorados:

- Administração básica de servidores Linux por SSH.
- Execução de serviços em contêineres Docker.
- Persistência de configurações e permissões de arquivos.
- Configuração de variáveis de ambiente e credenciais de API.
- Diagnóstico de erros de autenticação por meio de logs.
- Integração de um agente de IA com uma interface de mensagens.

## Próximos passos

1. Validar o planejamento diário pelo Telegram.
2. Integrar e testar as skills de estudos.
3. Implementar o registro estruturado das sessões.
4. Criar relatórios de desempenho e dificuldades.
5. Documentar testes, limitações e procedimentos de recuperação.

## Segurança

Credenciais, tokens do Telegram, chaves de API e arquivos de configuração com segredos não devem ser publicados no repositório.

## Status

Projeto em desenvolvimento. A infraestrutura inicial está configurada; as funcionalidades personalizadas de acompanhamento de estudos ainda estão em implementação.
