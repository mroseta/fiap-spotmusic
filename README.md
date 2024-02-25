# fiap-spotmusic

# Controle de Versionamento de Código

O uso do GitHub para versionamento de versões no projeto SpotMusic é crucial para garantir uma gestão eficiente do código-fonte e facilitar a colaboração entre os membros da equipe de desenvolvimento. A implementação do GitFlow para micro serviços proporciona uma metodologia estruturada para o gerenciamento de branches e releases, promovendo um fluxo de trabalho organizado e escalável.

O GitHub será utilizado como a plataforma principal para hospedar o repositório central do código-fonte do projeto SpotMusic. Todos os desenvolvedores terão acesso aos repositórios relevantes, onde poderão contribuir com novos recursos, correções de bugs e melhorias de forma colaborativa. O GitHub oferece recursos robustos para controle de versão, facilitando a rastreabilidade de alterações e a reversão de código quando necessário.

## Implementação do GitFlow para Micro Serviços

O GitFlow é uma metodologia de branching model que se adapta bem a projetos de grande escala, como o SpotMusic, que é baseado em micro serviços. A seguir, descrevemos os principais processos do GitFlow adaptados para o contexto de micro serviços:

### Branches Principais

- **Master**: Representa a versão de produção do sistema. Todo código neste branch é considerado estável e pronto para implantação.
- **Develop**: Branch de integração contínua, onde os desenvolvedores mesclam suas features após conclusão. Este branch é frequentemente implantado em ambientes de teste.

### Branches de Suporte

- **Feature**: Criado a partir do branch de develop, este branch é utilizado para desenvolver novas funcionalidades. Uma vez completada, a feature é mesclada de volta para o branch de develop.
- **Release**: Criado a partir do branch de develop, este branch é utilizado para preparar uma nova versão de produção. Aqui, são feitos os ajustes finais e testes antes da implantação no ambiente de produção.
- **Hotfix**: Branches criados a partir do branch de master para corrigir problemas críticos na produção. Uma vez corrigidos, são mesclados tanto para a master quanto para o develop.

### Processo de Desenvolvimento

- Os desenvolvedores criam branches de feature a partir do branch de develop para trabalhar em novas funcionalidades de forma isolada.
- Após a conclusão, a feature é mesclada de volta para o branch de develop através de um pull request.
- Periodicamente, uma nova release é criada a partir do branch de develop para agrupar funcionalidades concluídas e preparar para implantação.
