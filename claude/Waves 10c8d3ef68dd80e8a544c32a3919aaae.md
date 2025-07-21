# Waves

# Descrição

O sistema de **Waves** (ou Ondas) é responsável por estruturar os ataques inimigos em cada ataque do jogo. Ele define **pontos de origem**, **tipos e quantidades de inimigos**, além de controlar o **ritmo** e a **dificuldade** de cada ataque.

# Atributos

## Grupo de Inimigos

Um **Grupo de Inimigos** define uma configuração específica de inimigos que será enviada durante uma wave. Cada grupo determina:

- O **tipo de inimigo**
- A **quantidade**
- O **ritmo de aparição**
- O **ponto de origem** no mapa

# Fila de Grupos (WaveQueue)

Uma **Wave** é composta por uma sequência de Grupos de Inimigos. Essa fila representa a ordem em que os grupos serão ativados durante um ataque.

Exemplo visual de um Grupo de Inimigos:

![](https://t9009094518.p.clickup-attachments.com/t9009094518/bf523f36-4096-41b5-a9c3-46b6b53cd61d/imagem_2024-12-04_145650259.png)

Exemplo visual de uma Fila de Grupos:

![](https://t9009094518.p.clickup-attachments.com/t9009094518/4a93004d-918b-4063-b614-855af8fd7e81/imagem_2024-12-04_150055671.png)

# Funcionamento do Spawn

Para cada **Grupo de Inimigos**, os seguintes parâmetros são definidos:

- **Direção de Ataque**: A direção da qual os inimigos virão em relação ao centro da fábrica. Pode ser uma direção cardinal (Norte, Sul, Leste, Oeste) ou um ataque circular (360°), quando os inimigos surgem de todos os lados simultaneamente.
- **Ponto de Origem (Spawn Point)**: Coordenada inicial do grupo no mapa. Pode variar de acordo com a direção da wave.
- **Tipo de Inimigo**: Define o comportamento, velocidade, vida e habilidades da criatura.
- **Quantidade**: Total de unidades inimigas que serão enviadas.
- **Velocidade de Spawn**: Intervalo entre a aparição de cada unidade. Ex: 1.0 = uma unidade por segundo.
- **Tempo para Início (Delay)**: Tempo de espera antes do início desse grupo (em segundos).
- **Aguardar Finalização (Wait for Completion)**: Se true, o sistema espera esse grupo ser eliminado antes de ativar o próximo.

```
enemy_wave = function(_direction, _spawn_point, _enemy_type, _amount, _spawn_speed, _start_delay, _wait_completion) constructor {
  ...
}

wave_1 = new enemy_wave("norte", spawn_point_A, normal, 12, 1, 0, true);
wave_2 = new enemy_wave("norte", spawn_point_A, tank, 5, 0.5, 2, false);

wave_queue.add(wave_1, wave_2);

```

Esse código é apenas um exemplo do funcionamento do sistema, não é necessariamente para usar essa lógica apesar de eu recomendar construtor.

# Encerramento do Ataque

O ataque acaba quando:

1. Todos os grupos da fila foram ativados;
2. Todos os inimigos ativos foram derrotados.