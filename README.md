# miniguia-estudos-notebooklm
miniguia para estudos do notebooklm (curso DIO)

Contexto e Objetivos:
NotebookLM para explicar as principais diferenças entre as hyper-scooter disponíveis para compra no Brasil.

Curadoria de Fontes: 
Nami-BURN-E-USER-MANUAL
inmotion-rs-user-manual
dualtron-thunder-3-user-manual
kaboo-wolf-king-gtr-user-manual

Engenharia de Prompts e "Cicatrizes": 

Cenário 1: Comparativo de Performance e Modos de Condução
prompt 1 ("Qual a velocidade máxima de cada patinete?") Resposta 1: A IA poderia simplesmente retornar o número máximo absoluto sem contexto, ignorando que o Inmotion RS possui modos dinâmicos com limites diferentes e que o Kaabo possui uma limitação de fábrica específica
. Entendimento 1: deve ser feita uma estruturação mais rigorosa, a fim de não deixar a IA com "dúvida" do que ela deve te responder.
prompt 2 ("Compare a velocidade máxima e os diferentes modos de condução dos patinetes Dualtron Thunder 3, Inmotion RS e Kaabo Wolf King GTR, detalhando as limitações de velocidade de cada modo e restrições de fábrica, se houver.") Resposta 2: O Dualtron Thunder 3 atinge 100 km/h
. O Inmotion RS atinge 110 km/h, operando em 4 modos (Eco a 32 km/h, Normal a 64 km/h, Sport a 100 km/h e Extreme sem limite)
. O Kaabo Wolf King GTR é restrito a 25 km/h para se enquadrar na Classe 2
. Entendimento 2: Ao detalhar as variáveis (modos, restrições e limites de velocidade), forçamos a IA a analisar o contexto técnico real em vez de entregar apenas dados absolutos e secos.
Cenário 2: Mecanismos de Proteção contra Superaquecimento
prompt 3 ("O que acontece se o patinete esquentar muito? Quais são os códigos de erro?") Resposta 3: A IA poderia ser forçada a tentar inventar códigos de erro para modelos que não os possuem documentados dessa forma, gerando uma alucinação
. Entendimento 3: Nem todos os manuais utilizam "códigos de erro" tabulados (o Dualtron e o Kaabo tratam o superaquecimento em especificações gerais ou no display)
. O prompt induz ao erro por assumir antecipadamente uma premissa incorreta
.
prompt 4 ("Mapeie os mecanismos de segurança contra superaquecimento em cada modelo de patinete. Liste as temperaturas limites exatas que ativam a proteção e, caso o manual forneça, inclua os códigos de erro associados.") Resposta 4: O Dualtron Thunder 3 inicia proteção no BMS se a temperatura exceder 55°C
. O Kaabo possui proteção nativa a 120°C
. O Inmotion RS possui erros detalhados em tabela: 111/211 (placa controladora), 112/212 (motor), 114/214 (MCU) e 013 (bateria)
. Entendimento 4: O uso de condicionais de escape ("caso o manual forneça") aliado à exigência de limites exatos garante a extração de inteligência sem forçar a padronização, evitando que a IA crie dados inexistentes
.
Cenário 3: Acessibilidade e Segurança da Bateria
prompt 5 ("Mostre o passo a passo de como remover a bateria de cada um dos patinetes.") Resposta 5: A IA tentaria procurar e inventar um passo a passo genérico para todos os equipamentos, entregando um conselho perigoso para modelos em que isso é proibido
. Entendimento 5: Este é um "prompt indutor ao erro". Perguntar o "como remover" ignora se a ação é de fato permitida pelo fabricante. Para evitar riscos ao usuário, a instrução precisa ter um tom investigativo primeiro
.
prompt 6 ("Analise as diretrizes dos manuais sobre a acessibilidade da bateria para o usuário final. Indique claramente qual modelo permite a remoção da bateria e possui travas de segurança, e qual modelo proíbe a remoção, incluindo os riscos listados.") Resposta 6: O Kaabo Wolf King GTR foi projetado para bateria portátil com trava de senha de fábrica (000)
. O Inmotion RS adverte estritamente "Não remova a bateria", apontando o grande risco de incêndio caso desmontada
. O Dualtron Thunder 3 não aborda mecanismos de remoção para recarga avulsa
. Entendimento 6: Prompts instrucionais de análise comparativa com ressalvas impedem a recomendação de procedimentos de risco. Esse método extrai a melhor resposta, fundamentada na segurança operacional e diretrizes precisas das marcas


📚 MINIGUIA DE ESTUDO: Análise Técnica de Patinetes Elétricos de Alta Performance via Engenharia de Prompts
1. Resumos Estruturados do Assunto
A. Performance, Modos de Condução e Legislação A performance dos equipamentos não é definida apenas por sua potência absoluta, mas pelas configurações de modos e restrições legais:
Velocidade e Modos: O Inmotion RS atinge 110 km/h operando com 4 modos definidos (Eco a 32 km/h, Normal a 64 km/h, Sport a 100 km/h e Extreme sem limites)
. O Dualtron Thunder 3 chega a 100 km/h
. O Nami BURN-E apresenta 5 modos ajustáveis (E, D, S, C, X) e um modo Turbo que adiciona 12% de velocidade máxima
.
Limitações de Fábrica: Patinetes como o Kaabo Wolf King GTR e o Nami BURN-E vêm frequentemente limitados a 25 km/h, uma restrição programada para que se enquadrem nas diretrizes e categorias europeias de trânsito, como a Classe 2 (EN 17128)
.
B. Gerenciamento Térmico e Códigos de Falha O superaquecimento é um risco crítico nestes veículos de alta potência (72V a 84V), possuindo diferentes mecanismos de escape:
Níveis de Proteção: O Dualtron Thunder 3 possui um Sistema de Gerenciamento de Bateria (BMS) que aciona proteção automática quando a temperatura da bateria excede 55°C
. No Nami BURN-E, a proteção do controlador é configurável e atua ao atingir até 110°C, reduzindo a corrente e desabilitando o turbo
. O Kaabo possui proteção térmica nativa setada para 120°C
.
Mapeamento de Erros: O Inmotion RS adota um mapeamento granular tabulado. Erros como 111/211 indicam sobreaquecimento da placa controladora (MOS), 112/212 superaquecimento do motor, e 013 superaquecimento da bateria
.
C. Design Estrutural e Gestão da Bateria Os fabricantes tomam abordagens opostas sobre a intervenção do usuário em componentes críticos:
Baterias Removíveis vs. Proibidas: O Kaabo Wolf King GTR foi projetado para portabilidade, contando com uma bateria destacável (72V 35Ah) com alça e uma trava de segurança por senha (padrão 000)
. Em contraste, o manual do Inmotion RS traz um alerta estrito para que o usuário "não remova a bateria", citando riscos severos de incêndio em caso de desmontagem
.
Ajustes Estruturais: Modelos premium garantem ajustes finos mecânicos. O Inmotion RS permite ajustar a altura do chassi em quatro "engrenagens" (gears)
. O Nami BURN-E incorpora amortecedores de direção (steering dampers) para estabilizar o guidão
.
2. Glossário com os Principais Conceitos
BMS (Battery Management System): Componente de segurança vital que monitora a saúde da bateria, prevenindo curtos-circuitos, sobretensão, e cortando o sistema em altas temperaturas (ex: aos 55°C no Dualtron)
.
Engenharia de Prompts: O processo metodológico de estruturar comandos para a Inteligência Artificial. Envolve transformar perguntas vagas ("Qual a velocidade?") em instruções condicionais detalhadas para evitar omissão de contexto ou "alucinação" de dados
.
P-Settings / Configurações Avançadas: Menu nos displays TFT/LCD onde parâmetros operacionais do patinete são customizados (como força de arranque, limite de corrente por motor e força do freio eletrônico E-ABS)
.
Troubleshooting (Cicatrizes): No contexto de IA, é a etapa de analisar um prompt que falhou ou gerou erro, identificar o porquê da falha (a "cicatriz") e refinar a estrutura para o teste seguinte
.
Turbo Mode: Função presente no Nami BURN-E ativada via botão no guidão que, dependendo da temperatura, eleva a velocidade máxima em 12% suplementares, ignorando as restrições usuais
.
Steering Damper: Dispositivo cilíndrico de amortecimento de direção que pode ser ajustado ("+" para mais rígido, "-" para mais flexível) visando evitar oscilações perigosas na roda dianteira em altas velocidades
.
3. Prompts Reutilizáveis para Futuras Revisões
Abaixo estão frameworks de prompts, criados a partir dos aprendizados (troubleshootings) validados durante os testes, que você pode guardar e reutilizar para extrair informações precisas de manuais técnicos.
A. Prompt para Extração Analítica de Performance
Prompt: "Compare as métricas de performance (velocidade máxima, autonomia e capacidade da bateria em Wh/Ah) dos modelos [Inserir Modelos]. É mandatório detalhar as diferenças entre os diversos modos de condução eletrônicos e listar qualquer restrição mecânica ou limitação de fábrica ligada à legislação de trânsito." Por que funciona? Evita respostas binárias ou números fora de contexto, obrigando a IA a ler o manual em busca de categorias de trânsito (ex: EN 17128) e limitações configuradas pelo fabricante
.
B. Prompt para Mapeamento de Falhas e Sensores (Troubleshooting Técnico)
Prompt: "Consulte os manuais fornecidos e mapeie os mecanismos de segurança e alertas de falha para os componentes críticos (bateria, controlador e motores). Liste os limites exatos de temperatura de corte e construa uma tabela com os códigos de erro associados. Caso o manual de determinado modelo não utilize códigos numéricos tabulados, explique como o equipamento lida com a proteção." Por que funciona? A cláusula de escape condicional ("Caso o manual não utilize...") impede que a IA alucine ou tente forçar uma tabela de erros para equipamentos que só apresentam avisos em texto corrido
.
C. Prompt de Investigação Operacional e Segurança
Prompt: "Analise as diretrizes do fabricante sobre as intervenções do usuário final em peças críticas, como [inserir: Bateria / Ajuste de Suspensão]. Quais ações são expressamente proibidas e quais riscos o manual cita? Especifique também quais modelos possuem facilidades antifurto de fábrica ligadas a esses componentes (ex: travas por senha ou chaves de ignição)." Por que funciona? Uma pergunta de "como fazer" poderia fazer a IA listar um passo a passo perigoso. O tom de "análise de restrições" força a IA a buscar os avisos de perigo (como riscos de incêndio e perda de garantia) antes de repassar qualquer instrução
.
