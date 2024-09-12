# Análise Técnica do MVP Logo IA

## Maiores Desafios Técnicos

1. **Integração com API de IA**:
   - Estabelecer uma conexão Continua (evitar perda de prompts) e eficiente com a API de geração de imagens (Stable Diffusion).
   - Gerenciar tokens e níveis de prompt (quantidade de token que um prompt pode/deve gastar por imagem)

2. **Otimização de Prompts**:
   - Fine tuning prompt: Desenvolver um sistema para converter inputs do usuário em prompts eficazes (Analisar uso de um modelo simples de LLM para re-rescrever/incrementar os prompts).
   - Possivel ou não para o mvp seria implementar um mecanismo de feedback para melhorar a qualidade dos prompts ao longo do tempo (Isso entra como fine tuning porém não tenho certeza de como seria esse algoritmo).

3. **Processamento de Imagens**:
   - Implementar algoritmos para pós-processamento das imagens geradas (ajuste de cores, redimensionamento, check de estilo).
   - Garantir que o processamento seja rápido e eficiente (importante mesmo pro mvp, já que em tese rodariamos um processamento após o processamento da imagem).
   - Garantir que seja possivel a analise das imagens geradas (Estudar uso do `sketch` do stable diffusion).

4. **Gerenciamento de Dados**:
   - Criar o algoritmo que irá armazenar e organizar os logotipos gerados e seus metadados.
   - Implementar um mecanismo de busca eficiente para ícones e estilos pré-definidos.
   - Implementação desses estilos pré-definidos como uma base de dados para o Fine Tuning de Prompts.

5. **Escalabilidade**:
   - Projetar a arquitetura para lidar com múltiplas requisições simultâneas.
   - Otimizar o uso de recursos para manter os custos baixos (Important pelo custo de token de imagens no stable diffusion).

## Linguagem

Python é altamente recomendado para este projeto devido a:

- Ampla variedade de bibliotecas para processamento de imagens (PIL, OpenCV).
- Excelente suporte para integração com APIs e processamento de dados (Stable Diffusion, Claude).
- Forte ecossistema para machine learning e IA.


## Estimativa de Tempo

Considerando 3 horas por dia:

- Configuração inicial e planejamento: 2-3 dias
- Integração com API de IA (Functionamento total da relação de token e níveis de prompt): 3-4 dias
- Desenvolvimento do sistema de prompts: 5-7 dias
- Implementação do processamento de imagens: 4-6 dias
- Desenvolvimento do sistema de gerenciamento de dados: 3-4 dias
- Testes e refinamentos: Idealmente feito ao longo do desenvolvimento.

**Estimativa total: 22-30 dias (aproximadamente 1-1,5 meses)**

Essa estimativa é baseada na necessidade também do melhor estudo dos tópicos, além de que nem todos os tópicos precisam/podem ser feitos de uma vez:

e.g. A implementação do *sistema de prompts* e do *processamento de imagens*, dependem igualmente um do outro, portanto, podem ser implementados simultaneamente.
Gerando assim resultados mais rápidos de ser ver, mas que serão sempre incrementados/melhorados com o tempo/uso e testes
