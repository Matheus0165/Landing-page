#  Gestor de Portarias — Regras de Negócio (https://www.figma.com/design/SHiNxKwJlJu6TlMcI5McmS/LandingPagePortaria?node-id=0-1&t=s9TAsa3pXYAWxMwr-1)

## Informações do documento

**Autor(es):** Gilberto Ribeiro Junior, Matheus Varela de Paula, Zack Zayry  
**Data:** 07/06/2026  


---

## 1.  Resumo

Trata-se de um sistema para gerenciamento de portarias do **Instituto Federal Catarinense — Campus Videira**. O objetivo deste documento é registrar as principais regras de negócio, condições, usuários, permissões, fluxos e impactos relacionados ao sistema.

---

## 2.  Contexto e motivação

A instituição onde o sistema será desenvolvido é o **Instituto Federal Catarinense — Campus Videira**, localizado na cidade de Videira, no Meio-Oeste Catarinense. A instituição atua na oferta de formação educacional em diferentes níveis, incluindo cursos técnicos, tecnológicos, superiores, pós-graduação e cursos de curta duração.

Na organização administrativa do IFC, existem departamentos e setores importantes relacionados ao processo de portarias, como:

- Direção-Geral (DG);
- Diretoria de Administração e Planejamento (DAP);
- Diretoria de Ensino e Extensão;
- Gabinete Institucional, responsável pela elaboração e controle das portarias.

Além desses setores, outros usuários poderão ter acesso ao sistema em diferentes níveis de permissão, como servidores docentes e servidores técnicos, que poderão consultar e solicitar portarias.

O principal problema administrativo identificado é a **gestão das portarias**. Esse processo envolve desde a solicitação inicial até o vencimento da portaria e a conclusão da atividade designada. Os problemas secundários estão relacionados à elaboração, acompanhamento, publicação, arquivamento e controle da validade desses documentos.

No contexto administrativo, são observados dois atos principais no gabinete e na direção-geral:

1. Escrita de memorandos;
2. Elaboração de portarias.

Esses dois atos podem estar vinculados. Por exemplo, quando o campus recebe uma orientação via memorando da Reitoria, a Direção do campus pode determinar a execução da atividade por meio de uma portaria. Assim, uma portaria poderá estar relacionada a um ou mais memorandos que justificam sua criação.

---

## 2.1 Conceitos principais

### O que é uma portaria?

Uma **portaria** é um ato administrativo destinado a regulamentar, organizar e disciplinar procedimentos internos, definindo normas e diretrizes que devem ser observadas por órgãos, setores ou servidores competentes.

### Como uma portaria é composta?

Uma portaria é estruturada, geralmente, em três partes principais:

- **Parte preliminar:** identificação, número, data, ementa e autoridade responsável;
- **Parte normativa:** regras, determinações e disposições do ato;
- **Parte final:** vigência, assinatura, publicação e encerramento.

### Quais são as categorias de portaria?

As portarias podem ser classificadas em diferentes categorias, como:

- Normativa;
- Individual;
- Especial;
- Externa;
- Interna.

### Quais servidores podem participar de uma portaria?

Podem participar de uma portaria:

- Servidores efetivos;
- Servidores comissionados;
- Empregados públicos;
- Celetistas;
- Temporários;
- Servidores designados para comissões, grupos de trabalho, núcleos ou atividades específicas.

---

## 2.2 Responsabilidades e usuários

### Qual é o departamento responsável pela elaboração das portarias?

Em uma instituição de ensino, a portaria pode ser elaborada pela **Secretaria Administrativa**, pela **Direção-Geral** ou pelo **Gabinete Institucional**, com apoio do setor responsável pelo assunto tratado, como Ensino, RH, Coordenação ou TI. Depois, o documento deve ser assinado pela autoridade competente.

### Quem pode solicitar uma portaria?

A solicitação de uma portaria pode ser feita por setores, departamentos, chefias ou servidores que identifiquem a necessidade de formalizar uma decisão administrativa. Após a solicitação, o pedido deve ser analisado pelo setor responsável e aprovado pela autoridade competente.

### Quem pode assinar portarias?

Os servidores que podem assinar portarias são aqueles que exercem função de autoridade, coordenação ou designação formal dentro da instituição.

No contexto do sistema, os principais assinantes podem ser:

- Diretor-Geral;
- Coordenadores;
- Vice-coordenadores;
- Servidores autorizados formalmente, conforme o tipo de portaria.

---

## 2.3 Usuários, papéis e permissões


| Funcionalidade | Gabinete | DG | DAP | Ensino | Coord. | Vice | Docente | Técnico |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Consultar Portarias | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Solicitar Portaria | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Criar Portaria | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Editar Portaria | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Vincular Memorandos | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Aprovar Portaria | ✗ | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Assinar Portaria | ✗ | ✓ | ✗ | ✗ | ✓ | ✓ | ✗ | ✗ |
| Arquivar Portaria | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Emitir Relatórios | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ✗ |
| Gerenciar Usuários | ✓* | ✓* | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |

> **Observação:** permissões marcadas com `✓*` dependem de definição administrativa da instituição.

---

## 2.4 Fluxo de solicitação, elaboração, assinatura e publicação

O fluxo de uma portaria inicia com a solicitação feita por um setor ou servidor interessado. Em seguida, o setor administrativo analisa o pedido e elabora a minuta do documento. Após a revisão, a portaria é encaminhada para assinatura da autoridade competente. Depois de assinada, recebe numeração oficial, é publicada no meio adequado e arquivada para consulta e controle institucional.

```text
Solicitação
    ↓
Análise administrativa
    ↓
Elaboração da minuta
    ↓
Revisão administrativa ou jurídica
    ↓
Aguardando assinatura
    ↓
Assinatura da autoridade competente
    ↓
Publicação oficial
    ↓
Arquivamento
```

---

## 2.5 Cadastros necessários no sistema

Os cadastros necessários para o sistema de portarias são:

- Usuários;
- Departamentos;
- Cargos;
- Pessoas/servidores;
- Autoridades assinantes;
- Tipos de portaria;
- Modelos de portaria;
- Solicitações;
- Portarias;
- Revisões;
- Assinaturas;
- Publicações;
- Anexos;
- Histórico de tramitação.

Cada cadastro possui campos específicos para permitir o controle completo do fluxo, desde a solicitação até a publicação oficial da portaria.

---

## 2.6 Regras de negócio dos formulários

As principais regras de negócio a serem respeitadas em cada formulário são:

1. **RN-01:** Apenas usuários autenticados podem solicitar portarias.
2. **RN-02:** O título da portaria é obrigatório.
3. **RN-03:** A justificativa é obrigatória.
4. **RN-04:** Deve ser selecionada uma categoria válida:
   - Normativa;
   - Individual;
   - Especial;
   - Externa;
   - Interna.
5. **RN-05:** Pelo menos um responsável ou participante deve ser informado.
6. **RN-06:** Somente servidores cadastrados podem ser vinculados.
7. **RN-07:** Caso exista memorando relacionado, ele deve estar previamente cadastrado.
8. **RN-08:** A data de término não pode ser anterior à data de início.
9. **RN-09:** A solicitação deve iniciar com o status **Pendente de Análise**.

---

## 2.7 Relatórios solicitados

Os relatórios solicitados para o sistema de portarias são:

- Relatório de solicitações;
- Relatório de portarias emitidas;
- Relatório de portarias por departamento;
- Relatório de portarias por tipo;
- Relatório de pendências;
- Relatório de revisões;
- Relatório de assinaturas;
- Relatório de publicações;
- Relatório de histórico de tramitação.

Cada relatório deve apresentar informações como:

- Número da portaria;
- Solicitante;
- Departamento;
- Tipo;
- Assunto;
- Datas;
- Status;
- Responsáveis;
- Local de publicação.

---

## 2.8 Integrações com outros sistemas


| Sistema integrado | Função da integração |
|---|---|
| Sistema de usuários/servidores do IFC | Buscar dados dos servidores, cargos, setores, matrícula SIAPE e situação ativa/inativa. |
| Sistema de autenticação institucional | Permitir login com credenciais institucionais e controlar permissões por perfil. |
| Sistema de memorandos/documentos | Vincular um ou mais memorandos à portaria, usando número, data, assunto e órgão emissor. |
| Sistema de assinatura digital | Permitir assinatura oficial da portaria por Diretor-Geral, coordenadores ou usuários autorizados. |
| Sistema de protocolo/SEI/SIPAC, caso utilizado | Registrar, tramitar, protocolar ou consultar documentos oficiais vinculados à portaria. |
| E-mail institucional | Enviar notificações sobre solicitação, aprovação, rejeição, assinatura, vigência e vencimento. |
| Repositório/arquivo documental | Armazenar a versão final da portaria assinada e manter histórico para consulta e auditoria. |

---

## 2.9 Dados já validados considerados no sistema

Os dados já validados que deverão ser considerados no sistema são:

- Dados dos usuários;
- Departamentos;
- Cargos;
- Servidores envolvidos;
- Autoridades assinantes;
- Tipos de portaria;
- Solicitações;
- Portarias;
- Revisões;
- Assinaturas;
- Publicações;
- Anexos;
- Histórico de tramitação.

Esses dados precisam estar corretos, ativos e autorizados no sistema para garantir que a portaria seja solicitada, elaborada, assinada e publicada de forma segura e organizada.

---

## 2.10 Comissões, grupos de trabalho, núcleos e conselhos

### Conselhos e órgãos colegiados

- CONCAMPUS;
- CONSUPER;
- CODIR;
- CONSEPE.

### Comissões institucionais

- CPA;
- CPPD;
- CIS;
- Comissão de PPI, Ingresso, Matrículas e Baixa Renda;
- Comitê de Ensino;
- Comitê de Extensão.

### Núcleos institucionais

- NAPNE;
- NGA;
- NuPe;
- NEaD;
- AEE.

### Outros grupos institucionais

- APP;
- CLIFC.

---

## 2.11 Validade das portarias

O período de validade das portarias pode variar conforme o tipo do ato administrativo. Algumas portarias possuem validade indeterminada e permanecem em vigor até serem revogadas ou substituídas. Outras possuem prazo determinado, como portarias de comissão, eventos, grupos de trabalho ou substituições temporárias.

Também existem portarias vinculadas ao exercício de cargo ou função, que permanecem válidas enquanto durar a designação. Portanto, o sistema deve permitir diferentes tipos de validade, com campos para:

- Data de publicação;
- Início da vigência;
- Fim da vigência;
- Efeitos retroativos;
- Status;
- Eventual revogação.

---

## 2.12 Estados possíveis de uma portaria

Os estados possíveis de uma portaria no sistema são:

- Solicitada;
- Em análise;
- Criada ou minuta;
- Em revisão;
- Aguardando assinatura;
- Assinada;
- Publicada;
- Vigente;
- Atualizada;
- Retificada;
- Expirada;
- Revogada;
- Cancelada;
- Arquivada;
- Excluída.

A exclusão deve ser permitida apenas antes da publicação, pois portarias publicadas precisam permanecer registradas para manter o histórico e a rastreabilidade administrativa.

---

## 2.13 Alertas considerados no sistema

Os alertas que devem ser considerados no sistema de portarias são:

- Portarias próximas do vencimento;
- Portarias vencidas;
- Solicitações pendentes;
- Documentos aguardando revisão;
- Portarias aguardando assinatura;
- Portarias assinadas e ainda não publicadas;
- Solicitações devolvidas para ajustes;
- Portarias retificadas;
- Portarias revogadas;
- Ausência de anexos obrigatórios;
- Dados inconsistentes.

Esses alertas ajudam a controlar prazos, evitar atrasos, garantir a publicação correta dos documentos e manter a rastreabilidade do processo administrativo.

---

## 2.14 Documentos disponibilizados pela instituição

Os documentos disponibilizados pela instituição para compreensão do objeto principal do sistema são:

- Modelos de portarias;
- Portarias antigas já publicadas;
- Organograma institucional;
- Lista de departamentos;
- Lista de usuários e servidores;
- Cadastro de cargos e funções;
- Fluxo atual de solicitação e aprovação;
- Normas internas;
- Regras de assinatura;
- Documentos de publicação oficial;
- Políticas de segurança e proteção de dados;
- Relatórios utilizados atualmente;
- Planilhas de controle.

Esses documentos permitem compreender os dados que serão tratados pelo sistema, como nomes, cargos, matrículas, departamentos, assinaturas, anexos e datas de vigência. Também ajudam a demonstrar a relação entre funcionalidades como solicitação, elaboração, revisão, assinatura, publicação, consulta, alertas e relatórios.

---

## 3. Solução proposta

Para o desenvolvimento do sistema de gestão de portarias, algumas decisões principais foram definidas para garantir organização, segurança e controle do processo.

A primeira decisão é utilizar **controle por perfis de usuário**, permitindo que cada pessoa acesse apenas as funcionalidades relacionadas à sua função. Por exemplo, o solicitante poderá criar pedidos de portaria, o setor administrativo poderá analisar e elaborar a minuta, o jurídico poderá revisar, a autoridade poderá assinar e o publicador poderá realizar a publicação oficial.

Outra decisão importante é manter um **fluxo padronizado de tramitação**, evitando que a portaria pule etapas obrigatórias. Dessa forma, uma portaria só poderá ser publicada depois de assinada, e uma solicitação só poderá avançar quando possuir os dados obrigatórios preenchidos.

Também será necessário manter um **histórico de ações**, registrando quem criou, alterou, revisou, assinou, publicou ou revogou a portaria. Isso garante rastreabilidade e segurança administrativa.

Além disso, o sistema deverá possuir **alertas automáticos**, principalmente para portarias próximas do vencimento, solicitações paradas, documentos aguardando assinatura e portarias assinadas que ainda não foram publicadas.

### 3.1 Fluxo de trabalho proposto

```text
Solicitação da Portaria
        ↓
Análise Administrativa
        ↓
Elaboração da Minuta
        ↓
Revisão Administrativa/Jurídica
        ↓
Aguardando Assinatura
        ↓
Assinatura da Autoridade Competente
        ↓
Publicação Oficial
        ↓
Arquivamento e Acompanhamento
```

### 3.2 Como a solução aborda o problema

Essa solução resolve o problema da falta de controle no processo de portarias, pois centraliza todas as informações em um único sistema. Com isso, a instituição deixa de depender de planilhas, documentos soltos, e-mails ou controles manuais.

O sistema permite saber quem solicitou a portaria, em qual etapa ela está, quem precisa aprovar, quem assinou, quando foi publicada e qual sua situação atual. Isso reduz erros, evita perda de documentos, melhora a segurança das informações e facilita a consulta de portarias antigas.

Além disso, os alertas ajudam a evitar atrasos e esquecimentos, principalmente em casos de portarias próximas do vencimento ou aguardando assinatura. O histórico de tramitação garante transparência, pois todas as ações ficam registradas.

Portanto, a solução proposta aborda o problema por meio de:

- Padronização do processo;
- Controle de acesso;
- Automação de alertas;
- Registro de histórico;
- Segurança dos dados;
- Melhor acompanhamento das portarias.

---

## 4.  Alternativas consideradas

### Opção A: Manter o processo atual baseado em documentos e planilhas

O gerenciamento das portarias continuaria sendo realizado por meio de documentos editáveis, planilhas eletrônicas e armazenamento manual dos arquivos.

**Motivos para não escolher:**

- Dificuldade de localizar portarias antigas;
- Ausência de controle automático de vigência e vencimento;
- Maior risco de inconsistências e duplicidade de informações;
- Necessidade de trabalho manual para acompanhamento das portarias;
- Baixa rastreabilidade das alterações realizadas;
- Dependência do conhecimento dos servidores responsáveis.

### Opção B: Utilizar um sistema genérico de gestão documental

Foi considerada a utilização de ferramentas genéricas de gestão documental para armazenar e controlar os documentos relacionados às portarias.

**Motivos para não escolher:**

- Não contempla as regras específicas do processo de portarias do IFC;
- Necessidade de grande customização para atender aos fluxos institucionais;
- Dificuldade para controlar vigência, renovação e encerramento de portarias;
- Não possui estrutura adequada para gerenciamento de membros, comissões, conselhos e grupos de trabalho;
- Possível aumento de custos de implantação e manutenção.

---

## 5.  Avaliação de impacto

### 5.1 Dependências

Para que o Sistema de Gestão de Portarias funcione corretamente, será necessário contar com dados, definições e recursos previamente organizados pela instituição.

As principais dependências são:

- Cadastro atualizado de usuários do sistema;
- Cadastro de departamentos, setores e responsáveis;
- Cadastro de cargos e funções;
- Definição dos perfis de acesso;
- Modelos oficiais de portarias;
- Regras internas de solicitação, revisão, assinatura e publicação;
- Lista de autoridades que podem assinar portarias;
- Definição dos tipos de portaria;
- Regras de validade e vencimento;
- Política de segurança e controle de acesso;
- Infraestrutura para armazenamento dos documentos;
- Rotina de backup dos arquivos e dados;
- Treinamento dos usuários.

Também podem existir dependências externas, como sistema de assinatura digital, e-mail institucional para envio de notificações, site institucional para publicação ou integração com Diário Oficial.

### 5.2 Preocupações sobre migração ou implementação

Durante a implementação do sistema, uma das principais preocupações é garantir que os dados cadastrados estejam corretos. Caso usuários, setores, cargos ou autoridades sejam cadastrados de forma errada, o fluxo das portarias pode ser prejudicado.

Também é necessário cuidado com a migração de portarias antigas. Documentos já publicados devem manter suas informações originais, como número, data de emissão, data de assinatura, data de publicação, validade, status e arquivo final.

Pontos de atenção:

- Evitar duplicidade na numeração das portarias;
- Conferir se as portarias antigas ainda estão vigentes, expiradas ou revogadas;
- Garantir que os documentos migrados não sejam alterados indevidamente;
- Manter histórico das portarias já publicadas;
- Definir quais dados antigos serão importados para o novo sistema;
- Testar o fluxo antes da implantação oficial;
- Treinar os usuários antes do uso definitivo;
- Garantir que apenas usuários autorizados tenham acesso às informações.

A implementação pode ser feita por etapas, começando pelos cadastros principais e pelo fluxo básico de solicitação, elaboração, assinatura e publicação. Depois, podem ser adicionados relatórios, alertas, integração com assinatura digital e demais funcionalidades.

### 5.3 Riscos ou limitações

Durante a implantação do Sistema de Gestão de Portarias, alguns riscos devem ser considerados. Um deles é o **cadastro incorreto de dados**, como nomes, cargos, setores ou autoridades assinantes, o que pode gerar portarias com informações erradas. Para evitar isso, os cadastros devem ser conferidos e atualizados antes do uso do sistema.

Outro risco é a **duplicidade na numeração das portarias**. Como esse número é oficial, o sistema deve gerar a numeração automaticamente e impedir registros repetidos.

Também pode haver **resistência dos usuários**, já que alguns podem estar acostumados com planilhas, documentos em papel ou e-mails. Esse problema pode ser reduzido com treinamento e explicação do funcionamento do sistema.

A **migração de portarias antigas** também exige cuidado, pois documentos anteriores podem estar incompletos ou em formatos diferentes. Por isso, é importante revisar as informações antes de inseri-las no novo sistema.

Além disso, o sistema deve ter **controle de acesso**, garantindo que apenas usuários autorizados possam visualizar, editar, assinar ou publicar portarias. Também é necessário manter **backup dos dados**, para evitar perda de documentos importantes.

Por fim, podem ocorrer **atrasos na implementação**, principalmente se surgirem regras internas mais complexas. Para reduzir esse risco, o ideal é implantar o sistema por etapas, começando pelas funcionalidades principais.

### 5.4 Síntese da avaliação de impacto

As principais dependências do sistema são os cadastros atualizados de usuários, setores, cargos, autoridades assinantes, modelos de portaria, regras de assinatura, publicação e segurança.

As maiores preocupações na implementação estão relacionadas à migração de portarias antigas, validação dos dados, treinamento dos usuários, controle de acesso e prevenção de duplicidade de documentos.

Os principais riscos envolvem resistência à mudança, falhas na migração, erros de cadastro, acesso indevido, atrasos no cronograma e limitações técnicas. Esses riscos podem ser reduzidos com testes, implantação gradual, backup, validação das informações e controle de permissões.
