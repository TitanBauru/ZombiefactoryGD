# Ciclo de Dia e Noite

# Definição

O sistema de ciclo de dia e noite é o responsável pela passagem do tempo e também a mudança de estado entre dia e noite, contabilizando o número de noites sobrevividas com sucesso também.

# Funcionamento

## Tempo e contador de ciclos

O primeiro aspecto importante é o tempo, e ele é responsável por definir quanto tempo dura um dia e noite. Sempre que o jogador sobrevive a mais uma noite, o contador de ciclos aumenta. 

![image.png](image%2034.png)

<aside>
💡

O valor depende do balanceamento e de quanto tempo uma run deve durar. Ex: “Vampire Survivors” leva 30 minutos. Então para não quebrar o ritmo do Zombiefactory sugiro 5 minutos para cada ciclo.

</aside>

<aside>
💡

Titan “3 minutos o dia, 4 minutos a noite”.

</aside>

## Mudança de Estados

Existem 2 estados, dia e noite, o tempo atual é o responsável por chamar a troca de estados. As 5h59 da manha a noite acaba, e as 17h59 acaba o dia, repetindo mais um ciclo.

**Dia**: Durante o dia os zombies estão em menores números e o jogador pode aproveitar para explorar e melhorar a fábrica.

**Noite**: A noite é perigosa e é nesse momento em que o zombies vão atacar a fábrica com todas as suas forças.

# **Feedbacks**

Para a troca de dia e noite serão necessário diversos feedbacks:

- **Som para troca de estados**: Risk of Rain 2 tem um som característico para quando troca de estado de dificuldade.
 http://www.youtube.com/watch?time_continue=5&v=N3TpuxHjtaw&embeds_referring_euri=https%3A%2F%2Fwww.google.com%2Fsearch%3Fclient%3Dopera-gx%26q%3Drisk%2Bof%2Brain%2B2%2Bdificult%2Bchange%2Bsound%26sourceid%3Dopera%26ie%3DUTF-8%26oe%3DUTF-8&source_ve_path=Mjg2NjY 
https://www.youtube.com/watch?v=YB1tRbJvPkE
- **Animação para mudança no contador**: Sempre que o contador de ciclos completos aumentar, existe uma animação mostrando a mudança. 
https://www.youtube.com/watch?v=zaf7BW5juRY
- **Notificação**: Quando o jogador esta fora da fábrica e falta 2 horas para cair a noite ele recebe uma notificação “A noite esta chegando”.
    
    ![image.png](image%2035.png)