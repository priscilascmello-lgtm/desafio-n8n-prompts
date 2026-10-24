# Desafio Criativo: Planejando Automações com N8N Usando Apenas Bons Prompts

## Passo 1 – Definição da automação

Quero criar uma automação no N8N para processar automaticamente o status de operações recebidas por um sistema.

**Público ou responsável:**  
Equipe responsável pelo acompanhamento das operações e automações.

**Resultado esperado:**  
Identificar o status recebido, validar a situação da operação e direcioná-la automaticamente para a próxima ação correspondente.

---

## Passo 2 – Contexto e regras

**Ferramentas envolvidas:**  
N8N e um sistema de origem que envia os dados das operações.

**Fluxo desejado:**

1. Receber uma operação contendo seu identificador e status.
2. Ler e validar o status recebido.
3. Identificar qual ação deve ser executada de acordo com o status.
4. Direcionar a operação para a próxima etapa do processo.
5. Retornar o resultado do processamento.

**Regras importantes:**

- Se o status for `START`, a próxima ação deverá ser `VALIDATE`.
- Se o status for `PROCESS`, a próxima ação deverá ser `SAVE`.
- Se o status for `ERROR`, a próxima ação deverá ser `RETRY`.
- Se o status for `END`, a próxima ação deverá ser `FINISH`.
- Caso o status recebido não esteja entre os status previstos, a operação deverá ser direcionada para uma etapa de tratamento de erro.
- O fluxo não deve interromper o processamento das demais operações caso uma operação apresente um status inválido.

---

## Passo 3 – Prompt final

Atue como um especialista em N8N e automação de processos.

Crie uma automação no N8N para processar automaticamente o status de operações recebidas por um sistema.

**Público:**  
Equipe responsável pelo acompanhamento das operações e automações.

**Ferramentas envolvidas:**  
N8N e um sistema de origem que envia os dados das operações.

**Fluxo:**

1. Receber uma operação contendo seu identificador e status.
2. Ler e validar o status recebido.
3. Identificar a próxima ação de acordo com o status.
4. Direcionar a operação para a próxima etapa.
5. Retornar o resultado do processamento.

**Regras:**

- `START` → `VALIDATE`
- `PROCESS` → `SAVE`
- `ERROR` → `RETRY`
- `END` → `FINISH`
- Status desconhecido → `ERROR`

A automação deve ser organizada de forma clara e simples, permitindo fácil manutenção e entendimento do fluxo.

Explique quais nós do N8N devem ser utilizados, a função de cada nó e a lógica de funcionamento do workflow.

Apresente também um exemplo de entrada e o resultado esperado para cada status.