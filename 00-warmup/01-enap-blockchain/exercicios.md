# Exercícios — ENAP 0.1


## Módulo 1 — Definições
- Blockchain (linguagem simples):

Blockchain é uma cadeia de blocos (um registro) extremamente difícil de alterar.
Para mudar algo, seria quase impossível, porque exigiria o consenso da rede e de seus nodes. Após ser confirmado, o registro fica permanentemente gravado na rede.
Ela é segura e auditável, e pode ser mais transparente (em redes públicas) ou ter mais privacidade em algumas blockchains, mantendo sigilo de certos dados/transações, dependendo da tecnologia usada.

- Blockchain (linguagem técnica):
- Blockchain é uma estrutura de dados encadeada por HASHES, onde cada bloco agrega suas transacoes/dados e apontam para o hash do bloco anterior (se conversam), garantindo sua integridade e imutabilidade prática.
A ordem dos blocos e validade sao determinados pelo protocolo de consenso entre todos os nós (nodes), que são a rede.
Os (nodes) toleram falhas (BFT) dentro de limites, ou usam PoW/PoS. Assim, assegurando que a rede converge para um estado canonico.
Todas as transacoes sao autenticadas por suas assinaturas digitais (Public Key - criptografia de chave publica). As mesmas propagadas via rede P2P, conforme as regras de finalizaçao.
Em redes publicas, o ledger é verificavel por qualquer participante da rede (auditabilidade).
Enquanto em privacidade, pode variar de pseudonimidade a tecnicas como ZKPs, commitments, ring signatures ou transacoes confidenciais. Dependendo do protocolo/rede, camada e modelo de dados

  
- DLTs (resumo):
- DLTs - distribui um banco de dados em multiplos dispositivos.
o comum de um DLT é centralizar a informaçao em um ponto (tipo um servidor), e sincronizar a partir deste ponto.as atividades de todos os outros dispositivos conectados.
nem todas as redes DLTs sao blockchain, mas por ser baseada em uma cadeia de blocos sempre sera uma DLT.
Seria um registro distribuido. uma tecnologia em que um livro-razao/registro de dados e replicado e sincronizado entre seus nos (nodes) em vez de se marter em um servidor central.
Cada nó mantem uma copia, usa sistema de criptografia onde segue as regras para garantir integridade, consistencia e resistencia a adulteraçao.

  
## Módulo 2 — Centralizado / Descentralizado / Distribuído
Centralizado
Controle e validação ficam em uma entidade. Um dono decide regras, pode reverter ou pausar, bloquear e mudar saldos em alguns casos.
Resumindo: você confia no operador (custódia e decisões).
Exemplos:
Exchange custodial (Binance/Coinbase) e seus livros internos.
Banco de dados de um app cripto que “parece” blockchain, mas é só servidor.

Descentralizado
Controle e validação são distribuídos entre vários participantes independentes.
Não existe uma única entidade que consiga mudar as regras/estado sozinha.
Regras são aplicadas por consenso (miners/validators/nodes).
Censura e alterações arbitrárias ficam bem mais difíceis.
Exemplos:
Bitcoin (mineração + nodes verificadores).
Ethereum (validadores + nodes).
DEX (em rede pública), onde a execução é via contrato e consenso da rede.

Distribuído
Isso descreve a arquitetura de dados/infra, não “quem manda”.
O ledger (ou parte dele) é replicado em vários nós/servidores.
Pode existir em sistemas descentralizados (muitos nodes independentes).
E também pode existir em sistemas centralizados (vários servidores, porém um dono).
Exemplos:
Nodes completos guardando e replicando o histórico/estado.
Uma blockchain privada, dentro de um consórcio, pode ser distribuída, mas não necessariamente totalmente descentralizada.
---

## Módulo 3 — Adoção (Fácil)
Alguns mitos sobre a adoção de Blockchain (setor público/empresas).

1 "É caro implementar" — mito: existem estratégia e alternativas de bom custo-benefício para começar.

2 "Resolve tudo ou é única solução" — mito: não subestime a blockchain como solução principal de transformação.

3 "É sempre transparente" — mito: varia muito conforme a rede, desempenho e nível de permissão/abertura (não é automático).

4 "Segurança e privacidade são sempre ameaças" — mito: bem gerida, pode até simplificar conformidade e dar mais controle de dados.

5 "Dispensa regras, compliance e governança" — mito: contratos dentro da blockchain precisam conversar com regras fora dela.

POR QUE BLOCKCHAIN NÃO SUBSTITUI GOVERNANÇA/PROCESSO?

Blockchain é infra/registro, não "política pública". Mesmo com os smart contracts, as regras do mundo real (leis, contratos, papéis, auditoria, responsabilização e compliance) continuam existindo e precisam ser definidas fora da tecnologia e integradas a ela.
Sem processo bem desenhado (quem pode escrever/ler, como corrigir erros, como tratar exceções, como auditar e punir), você só troca um sistema ruim por um sistema ruim "carimbado" em blockchain.

DEFINIÇÕES DE REDES.

Rede pública.
Rede com acesso irrestrito para novos usuários. Em geral, tem mais sustentabilidade/participação (miners/usuários), mas não permite alto controle de um ator sobre os demais. Exemplos citados: Bitcoin e Ethereum.

Rede privada/permissionada.
Rede em que o acesso é permitido apenas a atores convidados/cadastrados pelos administradores. Em geral, depende mais de financiamento e, em troca, oferece mais controle de acesso e transparência (o quanto aparece para quem está fora).

Consórcio (quando faz sentido).
Arranjo em que várias organizações compartilham uma rede (muito comum porque criar redes novas é complexo, então juntar usos em redes existentes/consorciadas ajuda muito).
Faz sentido quando há múltiplos atores (cadeia de suprimentos) e você precisa de regras comuns, podendo ser sem fins lucrativos (financiado para desenvolvimento) ou com fim de remuneração por serviços.

### Médio
Checklist de adoção (toolkit)

1 Problema: descreva o problema real (dor, fraude, retrabalho, falta de rastreabilidade) e o resultado desejado.
2 Requisitos: liste requisitos funcionais e não funcionais (volume, tempo de resposta, integração, custo, disponibilidade).
3 Participantes: mapeie quem escreve, quem lê, quem valida, quem audita e quais incentivos cada ator tem.
4 Modelo de rede: escolha entre pública/privada, considerando que essa decisão afeta funcionalidade, segurança, compatibilidade e competitividade.
5 Governança: defina regras de entrada/saída de participantes, atualização de regras, gestão de chaves e responsabilidades (quem responde por quê).
6 Segurança: defina controle de acesso, gestão de chaves, redundância e requisitos de integridade/disponibilidade.
7 Privacidade: decida o que vai "on-chain" vs "off-chain", quem pode ver o quê e como cumprir LGPD (minimização/segregação de dados).
8 Auditoria: defina trilha de auditoria e como verificar registros; redes públicas bem estabelecidas tendem a facilitar verificabilidade (com trade-offs).
9 Piloto: isole a aplicação (escopo pequeno), faça protótipo/piloto e valide com usuários/órgãos parceiros.
10 Métricas: antes/depois (tempo de verificação, custo por verificação, redução de fraude, SLA, adoção, incidentes, interoperabilidade).

A escolha da rede

Rede pública.

Por quê? (3 motivos):

1 Auditabilidade e verificabilidade abertas: qualquer parte pode verificar, sem depender de um controlador único.
2 Interoperabilidade e padrões: redes públicas tendem a ser mais interoperáveis por comunidades diversas e código aberto.
3 Integridade reforçada por consenso aberto: redes públicas bem estabelecidas são citadas como mais apropriadas para assegurar integridade, com consenso distribuído e aberto.

Quais riscos estou aceitando?

1 Desempenho/latência e limitações de armazenamento: redes públicas, via de regra, tendem a ser mais lentas e não otimizadas para um caso específico.
2 Custos de transação variável: em redes públicas há taxas (fee) que podem flutuar conforme consumo/uso da rede.

### Difícil
"CASO"
Empresa/órgão querendo colocar uma infra de cadastro/registros interno em blockchain.

Uso da blockchain para cadastro/registro interno.

1. Problema e o que querem resolver?

- A dor principal, mais comum em "registro interno", geralmente vem de: trilha de auditoria fraca, alterações sem rastreio, baixa confiança entre áreas ou terceiros (quando há interações) ou dificuldade de provar "quem alterou o que e quando".

- O resultado desejado deve ser: garantir integridade do histórico (sem adulterações), rastreabilidade, auditoria rápida e redução de divergências ou contestações.


2. Perguntas obrigatórias antes de escolher uma blockchain
1. Quantas pessoas vão escrever os registros? Uma área só ou várias áreas/empresas?
2. Existe baixa confiança entre os participantes?
3. Qual é o nível de sensibilidade dos dados? LGPD, sigilo, dados pessoais e segredo industrial?
4. Quais os campos que precisam de imutabilidade e quais podem ser corrigidos? Erros, restrições ou cancelamentos?
5. Qual seria o volume e a frequência de gravações/consultas? TPS, picos e SLA.
6. Quem vai auditar e com qual frequência? Interno, externo e órgão de controle.
7. Quais as integrações que existem? ERP, sistemas legados? E quem é o dono dos dados?
8. Qual é a exigência de governança? Regras de acesso, papéis, atualizações de regras e gestão de chaves.
9. Quais são os custos aceitáveis e horizonte de manutenção? Operação, times e suporte.
10. Precisa de verificabilidade pública? Cidadão, cliente, fornecedor conferindo autenticidade.

3. Avaliação técnica

- Faz algum sentido usar a blockchain?

1. Se for interno e apenas um único dono confiável, a blockchain costuma ser um overkill. Um banco e auditoria forte resolve fácil.
2. Se tiver sistemas, áreas, entidades gravando e existir conflito ou risco de adulteração, aí a blockchain pode agregar valor.
3. Benefício apenas para confiança e prova de integridade, não armazenamento de dados.
4. Qual modelo de rede usar e por quê?

- Permissionada ou consórcio, se houver mais de uma organização.

Por quê?

1. Controle total de acesso e segregação. Registro interno: dados podem ser sensíveis à LGPD.
2. A questão da governança clara: quem escreve, valida e audita; facilidade de operar SLA internamente.
3. Custos e previsibilidades melhores que a rede pública para caso interno: taxas e latência mais previsíveis.

- O que vai on-chain e off-chain

1. On-chain: hash, metadados, ID, timestamp, versão, órgão e tipo de evento, URL e status (ativo, retificado e cancelado).
2. Off-chain: dados completos, pessoas e documentos, anexos, conteúdos sensíveis, campos que exigem retificação frequente.
5. Alternativa mais adequada com auditoria

- Banco de dados, logs imutáveis (WORM/append-only), assinaturas digitais, trilha de auditoria, controle de acesso, carimbo do tempo, backups e segregação.

Por que resolve:

1. Menor custo e complexidade, mantém auditoria forte e com rastreabilidade.
2. Facilita LGPD sem congelar dados em um ledger.
3. Desempenho e relatórios internos melhores.

6. Um plano piloto

1. 2 a 4 semanas: escolher 1 tipo de registro, modelar eventos (criar, alterar ou retificar), provar o hash, assinatura e a validação.
2. 4 a 8 semanas: de 2 a 3 áreas usando, interação mínima com sistema legado, auditoria mesmo que simulada.
3. Validar e escalar: revisão de governança, segurança, chaves, LGPD, custo de operação; decidir expandir ou trocar por alguma alternativa.

7. Todas as métricas de sucesso

1. Tempo de auditoria e verificação: antes e depois; redução de retrabalho.
2. Incidentes de alteração e divergências não autorizadas: queda e rastreabilidade completa.
3. Adoção e SLA: percentual de registros, disponibilidade e latência.

---

## Módulo 4 — Aplicações (Fácil)

BNDESToken
TCU (levantamento/estudo sobre blockchain)
b-CPF / b-CNPJ

### Médio
Escolher 1 caso — BNDESToken

Objetivo
Aplicar a blockchain para dar mais controle, rastreabilidade e confiança em operações de repasse ou transferência de recursos de crédito do BNDES.
Modelo de rede que faz mais sentido (pública / permissionada / consórcio)
Permissionada ou consórcio permissionado, porque envolve atores identificados (BNDES e entidades tomadoras), com necessidade de governança e controle de acesso de operações institucionais.
Principal risco
Governança, adoção e integração: se regras, papéis e integração com sistemas legados não forem bem definidos, você cria complexidade sem ganho real (blockchain “carimba”, mas não substitui o processo).

### Difícil
“Real Digital”

O Real Digital aparece no contexto de blockchain porque é uma iniciativa inspirada em tecnologias blockchain para criar uma CBDC (moeda digital do banco central).
O curso enfatiza que ele é baseado em blockchain e se relaciona ao conceito de stablecoin (buscando estabilizar valores via lastro e estrutura), diferenciando de criptoativos públicos como o Bitcoin/Ether por ter camadas fechadas e restritas e controle do banco central em algum nível.
Os benefícios possíveis podem incluir modernizar infraestrutura de pagamentos e liquidação, ampliar eficiência e inovação na parte financeira e aproximar a confiança do sistema monetário do usuário final, mantendo atributos de confiança do banco central.
Riscos e limitações: privacidade e desenho de identificação ou anonimato (o texto discute formas de dinheiro digital com diferentes graus de identificação).
Centralização operacional, com camadas controladas pelo Banco Central. Além disso, há o tema de percepção e credibilidade no contexto do “inverno cripto”, onde crises (stablecoins, exchanges e regulações) afetaram a confiança no ecossistema e a percepção de blockchain em geral.
