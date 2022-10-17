# AWS Certified Cloud Practitioner (CLF-C01)

O exame AWS Certified Cloud Practitioner (CLF-C01) destina-se a pessoas que podem demonstrar
efetivamente um conhecimento geral da Nuvem AWS, independentemente de uma função de trabalho
específica.

#### O exame valida a capacidade de um candidato de concluir as seguintes tarefas:

- Explicar o valor da Nuvem AWS
- Compreender e explicar o modelo de responsabilidade compartilhada da AWS
- Entender as práticas recomendadas de segurança
- Compreender as práticas de faturamento, economia e custos da Nuvem AWS
- Descrever e posicionar os principais serviços da AWS, incluindo computação, rede, bancos
  de dados e armazenamento
- Identificar serviços da AWS para casos de uso comuns

### Descrição do Candidato

O candidato deve ter seis meses, ou o equivalente, de envolvimento ativo com a Nuvem AWS, com
exposição ao design, à implementação e/ou às operações da Nuvem AWS. Os candidatos deverão
demonstrar uma compreensão das soluções bem projetadas da Nuvem AWS.

#### Conhecimento recomendado da AWS

O candidato deve ter os seguintes conhecimentos:

- Conceitos da Nuvem AWS
- Segurança e conformidade na Nuvem AWS
- Compreensão dos principais serviços da AWS
- Compreensão da economia da Nuvem AWS

# Computação em nuvem

- É a entrega de recursos de TI sob demanda pela internet com uma definição de pagamento pelo que usa.

# Entrega sob demana

- Ter os serviços quando precisar e de imediato

# Infraestrutura da AWS

- Região
- Zona de disponibilidade
- Ponto de presença

# Região

- É composta por 2(duas) ou mais zonas de disponibilidade

# Fatores consideráveis ao escolher uma região

- Latência -> tempo em que os dados são enviados e recebidos
- Custo -> valor do serviço
- Serviços disponíveis -> os serviços presentes naquela região
- Compliance -> seus dados podem estar naquela região?
- Proximidade -> Onde você tem mais clientes?

# Zonas de disponibilidade

- É um cojunto de datacenters, altamente redundantes projetados para trabalhar de forma isolada em caso de falha em alguma outra AZ.
- Situados geograficamente distantes umas das outras
- Interconectadas através de uma rede de telecom de Baixa Latência
- É composta por 1(um) ou mais datacenter, recomenda-se 2(dois) ou 3(três) datacenters.
- AWS possui atualmente 84 zonas de disponibilidade em 26 regiões

# Ponto de presença

- É um datacenter com escopo de serviço reduzido
- AWS possui atualmente, mais de 410(quatrocentos e dez) pontos de presença em todo mundo

# Ecopo de serviço

- Define se o serviço roda apenas dentro de uma zona de disponibilidade, de uma região ou globalmente.

# Níveis de escopo de serviço

- Zona de disponibilidade
- Região
- Global

# Modelo de responsabilidade compartilhada

- É uma matriz de responsabilidade entre a AWS e o Cliente-AWS, divida em Responsabilidade da Nuvem e Responsabilidade na Nuvem

# Responsabilidade da Nuvem é da AWS

- Hardware, software, rede, datacenter

# Responsabilidade na Nuvem é do Cliente-AWS

- Sistema operacional e serviços que rodam no mesmo
- Rede (LAN, WAN)
- Firewall
- Criptografia de dados

# IAM Identify And Acces Manegement

- Serviços AWS que gerencia usuários, grupos e permissões de acesso aos recursos do ambiente.

# Entidade IAM

- Usuários
- Grupos
- Policies

# Boas práticas IAM

- NUNCA use a conta root!
- Crie usuários individuais, nada de usuários compartilhados
- Use o conceito de menor privilégio
- Conceda permissões para grupos, não para usuários
- Configure uma política de senhas
- Habilite MFA em todas as contas administrativas
- Para aplicações que rodam em EC2, use roles
- Rotacione suas credenciais regularmente
- Use CloudTrail para manter histórico de atividades em sua conta

# VPC Virtual Private Cloud

- Habilita recursos da AWS dentro de uma rede virtual, completamente apartada e exclusiva
- Semelhante a um ambiente de rede no modo tradicional

# Recursos de uma VPC

- Route table
- Internet Gateway - fornece acesso à internet
- Virtual Private Gateway - fornece acesso ao seu ambiente On-premisse
- Nat Gateway(Nat Instance) - fornece acesso à internet para as instâncias, mesmo que elas não tenham end. ip público
- Security groups - fornece controle do tráfego inbound e oubound
- ACL (Network Acces Control List) controla o tráfego de entrada e saída de uma subnet

# Subnet

- Segmentação de endereçamento de rede dentro de uma VPC
- Maior range: /16 256 subnet 65534 Ip's
- Menor tange /128 + 1 milhão de subnet 14 Ip's

# Endereçamento ip Subnet

- 10.0.0.0 Network address
- 10.0.0.1 Reservado para roteador da VPC
- 10.0.0.2 Reservado para serviço de DNS
- 10.0.0.3 Reservado para uso público
- 10.0.0.4 - 1.0.0.254 Disponíveis para uso
- 10.0.0.5 Network Broadcast Address

# ENI(Elastic Network Interface)

- É a interface de rede virtaul da instância

# Elastic IP

- É um endereço de ip público que reservado para sua conta AWS. Tem-se o controle de mapear e reutilizar em outras instâncias
- Tem escopo de serviço de região pode-se usar em todas suas regiões

# Público IP

- É aleatoriamente designado à sua instância no momento da inicialização. Não tem-se controle e não pode ser mapeado em outras instâncias
