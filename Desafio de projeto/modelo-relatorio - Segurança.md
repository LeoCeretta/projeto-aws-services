# RELATÓRIO DE IMPLEMENTAÇÃO DE MEDIDAS DE SEGURANÇA

- Data: 28/06/2024
- Empresa: Abstergo Industries 
- Responsável: Leonardo Dallepiane Ceretta

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Leonardo Dallepiane Ceretta. O objetivo do projeto foi elencar 3 medidas de segurança em conjunto dos serviços da AWS, com a finalidade de realizar aumentar a segurança na empresa.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 medidas de segurança. A seguir, serão descritas as etapas da implementação:

## Medida 1: 
- AWS Key Manegement Service (KMS).

AWS Key Management Service (KMS) é um serviço gerenciado que facilita a criação e o controle das chaves criptográficas usadas para proteger os dados. Ele oferece uma série de benefícios significativos em termos de segurança, conformidade e gerenciamento de chaves. Podemos destacar os principais deles como:
1. Controle de acesso detalhado:
    - Uitilizando uma política de controle de acesso, a empresa poderá definir políticas detalhadas que atendam seus requisitos e controlar quem tem acesso às chaves e como elas podem ser usadas;
    - O KMS se integra facilmente com o IAM (Identity and Acess Management), permitindo uma gestão centralizada de permissões.
2. Segurança avançada:
    - O KMS permite a criptografia de dados em repouso e em trânsito, garantindo que os dados estejam protegidos mesmo que sejam interceptados;
    - As chaves são armazenadas em módulos de segurança de hardware que são certificados e auditados para garantir a integridade e segurança.
3. Alta disponibilidade e escalabilidade:
    - O KMS é um serviço gerenciado pela AWS altamente disponível, e isso significa que a empresa, ao utilizá-lo, não precisa se preocupar com a infraestrutura subjacente;
    - O serviço é projetado para escalar de acordo com a demanda, sem a necessidade de intervenção manual.

Como um exemplo de caso de uso, podemos pensar que empresa farmaceutica Abstergo Industries precisa garantir a segurança dos dados sensíveis armazenados em seu banco de dados, informações essas como transações financeiras, dados de clientes entre outras. A empresa deseja criptografar esses dados para proteger contra acesso não autorizado. Para isso, utilizará o AWS KMS como parte da solução.

O processo dará inicialmente com criação de chaves que serão usadas para criptografar e descriptografar os dados sensíveis no banco de dados. Após, haverá uma integração com o RDS, que nada mais é que o banco de dados relacional que a empresa está hospedando seus dados, assim o RDS utiliza as chaves do KMS para criptogragar os dados em repouso, garantindo que todos os dados armazenados sejam automaticamente criptogragados. Além disso, pode-se definir políticas de controle de acesso no KMS, garantindo que apenas administradores autorizados possam gerenciar as chaves. Por fim, o KMS pode ser integrado com o AWS CloudTrail que tem o papel de monitorar todas as operações realizadas com as chaves do KMS, garantindo segurança e detecção de atividades suspeitas.

Como resultado, a empresa consegue proteger seus dados sensíveis de forma eficiente, cumprindo com os requisitos de conformidade e reduzindo o risco de vazamento de informações. A integração com o AWS KMS simplifica a gestão das chaves e garante que a segurança dos dados seja mantida sem comprometer a performance ou a usabilidade.


## Medida 2: 
- AWS Shield.

AWS Shield é um serviço gerenciado que oferece proteção contra ataques de negação de serviço distribuído (DDoS). Existem duas versões: *AWS Shield Standard* e *AWS Shield Advanced*, cada uma com um conjunto de funcionalidades voltadas para diferentes níveis de proteção. Podemos destacar os principais deles como:
1. Proteção contínua e automática:
    - O AWS Shield oferece monitoramento contínuo e proteção automática contra ataques DDoS, preduzindo o impacto sobre a disponibilidade dos seus serviços;
    - A resposta do AWS Shield é automátca para ataques conhecidos, ou seja, não há necessidade de intervenção manual, o que garante uma resposta rápida e eficiente.
2. Escalabilidade e resiliência:
    - A infraestrutura AWS é projetada para escalar automaticamente em resposta a picos de tráfego, ajudando a absorver e mitigar ataques DDoS volumétricos;
    - A arquitetura distribuída e redundante da AWS melhora a resiliência contra ataques e aumenta a disponibilidade dos seus aplicativos.
3. Visibilidade e relatório:
    - O AWS Shield em seu formato pago (AWS Shield Advanced) fornece relatórios detalhados sobre tentativas de ataques e medidas de mitigação, permitindo uma visão clara sobre a segurança de suas aplicações;
    - As ferramentas de análise disponibilizadas pelo AWS Shield ajudam a identificar padrões de tráfego suspeitos e a ajustar políticas de segurança para uma melhor proteção.
4. Integração com outros serviços AWS:
    - O AWS Shield se integra facilmente com outros seviços AWS, tais como o CloudFront, Route 53, Elastic Load Balancing (ELB) entre outros, proporcionando uma camada de defesa robusta e abrangente.

Como um exemplo de caso de uso, voltamos a pensar em nossa empresa do ramo farmacêutico Abstergo Industries, a mesma, possui um site de alta visibilidade que é alvo frequente de tentativas de ataques DDoS, esses ataques tem o potencial de causar interrupções no serviço, resultando em perda de vendas de seus produtos bem como danos à sua reputação. Como solução, a empresa resolveu utilizar o AWS Shield para proteção eficaz contra esses ataques, garantindo assim disponibilidade contínua de seu site para seus clientes.

O processo de implementação começará pela escolha da utilização avançada do serviço, ou seja, o AWS Shield Advanced, o mesmo traz benefícios extras quando comparado com a versão Standard, além de fornecer proteção adicional contra ataques DDoS, também fornece um suporte especializado. Além disso, será feita uma integração do AWS Shield Advanced com o CloudFront, outro benefício da escolha da versão paga, uma vez que a versão Standard não possui integração com o CloudFront, e com isso, a empresa terá garantia de uma defesa contra ataques DDoS distribuídos geograficamente, ou seja, terá uma capacidade de mitigar ataques volumetricos nos pontos de presença globais da empresa. Por fim, com o uso do AWS Shield Advanced, a empresa terá alertas em tempo real sobre as tentativas de ataques bem como relatórios detalhados que ajudam a entender melhor o tráfego e a efcácia das medidas de mitigação.

Como resultado, a empresa consegue manter a disponibilidade do seu site mesmo durante ataques DDoS significativos, minimizando o impacto sobre os negócios e garantindo uma experiência de usuário consistente e confiável. A visibilidade aprimorada sobre os ataques e o suporte especializado proporcionam uma camada adicional de segurança que ajuda a proteger a reputação e a receita da empresa.


## Medida 3: 
- Amazon GuardDuty

O Amazon GuardDuty é um serviço de detecção de ameaças que monitora continuamente suas contas da AWS, redes e cargas de trabalho em busca de atividades maliciosas ou comportamentos anômalos. Ele utiliza machine learning, análise de comportamento e fontes de inteligência de ameaças para identificar possíveis riscos. Podemos destacar os principais deles como:
1. Detecção avançada de ameaças:
    - O GuardDuty utiliza algoritmos avançados de machine learning para analisar o tráfego de rede e os logs de eventos, identificando atividades suspeitas ou anômalas que podem indicar uma ameaça;
    - Também consegue se integrar com fontes de inteligência de ameaças da AWS e outras bases de dados de segurança, para identificar e correlacionar indicadores de comprometimento em tempo real.
2. Monitoramento contínuo e automatizado:
    - O GuardDuty monitora continuamente suas contas, redes e recurnos, em uma escala 24/7, garantindo que você seja notificado de atividades suspeitas a qualquer hora do dia;
    - Também pode ser configurado para responder automaticamente a ameaças detectadas, por exemplo, é capaz de isolar uma instância comprometida ou bloquear um endereço IP malicioso.
3. Relatórios e análises detalhadas:
    - O Amazon GuardDuty gera relatórios detalhados sobre as ameaças detectadas, incluindo a origem, o tipo de ameaça e a recomendação de mitigação;
    - Além disso, as ferramentas de visualização disponíveis no GuardDuty, ajudam a entender melhor os padrões de ameaças e a tomar decisões informadas sobre a segurança da infraestrutura em questão.
4. Integração com outros serviços AWS:
     - O GuardDuty se integra facilmente ao AWS Scurity Hub e fornece uma visão centralizada das ameaças ajudando assim na gestão da segurança em toda a organização;
     - Analisa automaticamente os logs do AWS CloudTrail e os registros de fluxo da VPC para identificar atividades suspeitas.

Como um exemplo de caso de uso, a Abstergo Industries utiliza várias contas da AWS para diferentes projetos e serviços. Em uma dessas contas, um desenvolvedor acidentalmente expôs suas credenciais de acesso ao repositório de código público, criando um risco de segurança potencial, pois atacantes podem tentar usar suas credenciais para acessar os recursos da empresa na AWS.

A solução para esse problema inicia-se com a ativação do Amazon GuardDuty em todas as contas da AWS da empresa, para garantir o monitoramento contínuo e a detecção de ameaças. O GuardDuty então analisa os logs do AWS CloudTrail e os registros de fluxo da VPC para detectar atividades suspeitas, como tentativas de login não atorizados e alterações de políticas de segurança ou acessos a dados sensíveis. Após o processo de análise, o GuardDuty detecta uma série de tentativas de login usando as credenciais expostas, isso aciona um alerta de atividade suspeita, indicando um possível comprometimento da conta. Por fim, o GuardDuty envia uma notificação detalhada à equipe de segurança da empresa, incluindo informações sobre a origem do acesso, a localização geográfica e as ações realizadas. A empresa decide então isolar a conta comprometida e revogar as credenciais expostas.

Como resultado, a empresa detecta rapidamente o acesso não autorizado e toma medidas eficazes para mitigar o risco, evitando possíveis danos maiores, como a exposição de dados sensíveis ou interrupções nos serviços. A utilização contínua do Amazon GuardDuty proporciona uma camada adicional de segurança proativa, ajudando a proteger os recursos da empresa contra futuras ameaças.

## Conclusão
A implementação destas ferramentas na empresa Abstergo Industries tem como esperado uma postura de segurança robusta e abrangente para a infraestrutura e operações da empresa na AWS. O que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.


## Assinatura do Responsável pelo Projeto:

Leonardo Dallepiane Ceretta