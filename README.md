# PB-atividade-final

## Escopo
Neste projeto visamos uma nova solução para o e-commerce da **Fast Engineering S/A**. Essa arquitetura tem como objetivo ampliar a capacidade dos servidores, a fim de sustentar a crescente demanda de clientes, a qual está enfrentando um acréscimo aproximado de **20% mensalmente**.
## Arquitetura
![259829520-4e1a5c27-b343-4477-9435-bbef8ef08d17](https://github.com/vitortoniolo/PB-atividade-final/assets/133904035/470b4e33-1a3d-4830-b5a9-2075742ab581)

- **EKS:**
A base dos servidores será via Kubernetes, o qual será gerenciado pelo serviço EKS. O uso do EKS proporciona diversas vantagens, tais como maior simplicidade na administração, compatibilidade com outros recursos, escalabilidade e alta disponibilidade.
O EKS será responsável por orquestrar os nodes e, consequentemente, o servidor web e a aplicação. Graças à natureza da arquitetura do Kubernetes, o ambiente será altamente disponível, resistente a falhas e permitirá a aplicação realizar atualizações sem downtime.
- **Banco de dados RDS MySQL:**
O serviço RDS será utilizado para hospedar o banco de dados MySQL. O uso do RDS proporciona diversas vantagens, como gerenciamento automatizado, escalabilidade e backups automáticos.
- **Armanezamento EBS:**
O EBS servirá para armazenar todos os dados estáticos dos contêineres, permitindo acesso rápido e persistência dos dados necessários para o servidor web.
- **Multi AZ:**
Todos os recursos relevantes serão hospedados em duas zonas de disponibilidade, o que concede alta resiliência ao sistema e o protege de possíveis quedas.
- **Balanceamento de carga:**
Também será utilizado o ELB para distribuir a carga entre as instâncias dos contêineres, além de realizar health checks na conexão para prevenir quaisquer problemas.
- **Segurança:**
Serão configurados grupos de segurança da AWS para restringir o acesso apenas aos serviços e portas necessários, garantindo a segurança do ambiente. Além dos grupos de segurança, o IAM também será configurado para gerenciar as permissões e o acesso aos recursos da AWS. Serão criados grupos de usuários e políticas de acesso que permitem apenas o mínimo necessário para cada serviço e função na empresa.
- **Route 53:**
O Route 53 será responsavel por direcionar o tráfego para o ELB, e também provisionará o registro de dominio para o servidor. 

### Valores
| Mensal  | Anual  |
| ------------ | ------------ |
| 755.00 USD  | 9,070.00 USD  |
| 3.700,00 R$  | 44.500,00 R$   |

### Prazo de entrega:
Para a realização e implementação integral dos serviços oferecidos pela empresa Fast Engineering S/A, estima-se que seja necessário um período aproximado de **duas semanas.**

### Cronograma de macro-integras:
- Prova de conceito (POC): A POC servirá para validar a arquitetura criada, expondo possíveis falhas e indicando possíveis mudanças antes de criarmos o MVP. Para a prova de conceito será necessário **3 dias e meio.**
- Mínimo produto viável (MVP): Na MVP, teremos apenas os recursos mínimos, com suas funcionalidades básicas, sendo assim uma versão enxuta do Produto final. Para a criação do Mínimo produto viável será necessário** 3 dias e meio.**
- Produto final: O produto final será a implementação da arquitetura apresentada. Para construir a arquitetura apresentada, será necessário aproximadamente **uma semana.**
