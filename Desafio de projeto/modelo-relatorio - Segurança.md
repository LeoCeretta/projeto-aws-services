# RELATÓRIO DE IMPLEMENTAÇÃO DE MEDIDAS DE SEGURANÇA

Data: 28/06/2024
Empresa: Abstergo Industries 
Responsável: Leonardo Dallepiane Ceretta

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

Medida 2: 
- AWS Shield.



Medida 3: 
- Amazon GuardDuty
- [Descrição de caso de uso]


## Conclusão
A implementação de ferramentas na empresa *[nome da empresa] tem como esperado [benefícios das ferramentas]*, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

[lista de anexos, como manuais, documentos, planilhas, entre outros]

Assinatura do Responsável pelo Projeto:

Leonardo Dallepiane Ceretta