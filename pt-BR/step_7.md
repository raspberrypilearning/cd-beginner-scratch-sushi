## Peixe de controle remoto

Ok, agora é hora de fazer o peixe nadar sozinho. Para fazer isso, você vai precisar de um novo tipo de bloco: um bloco **Controle**.

\--- task \---

Selecione seu ator peixe.

Arraste um bloco `quando ⚑ for clicado`{:class="block3events"} da seção **Eventos**, um bloco `sempre`{:class="block3control"} da seção **Controle**, e um bloco `mova 10 passos`{:class="block3motion"} da seção **Movimento** para dentro do **painel do ator**, assim:

```blocks3
    when green flag clicked
    forever
        move (10) steps
    end
```

\--- /task \---

## \--- collapse \---

## title: O que o novo bloco faz?

Blocos de **Controle** fazem seu programa fazer as coisas um certo número de vezes ou sob certas condições.

Aqui, o peixe faz o que está dentro do bloco `sempre`{:class="block3control"} repetidamente em um loop, para sempre. Então, uma vez que tenha feito a última coisa (bloco) dentro do bloco `sempre`{:class="block3control"}, começa de novo no topo e faz tudo de novo, e assim por diante.

\--- /collapse \---

\--- task \---

Agora clique na bandeira verde e veja o que acontece!

\--- /task \---

Bem, esse peixe simplesmente colidiu com o lado do Palco, e estava se movendo rápido demais para o seu tubarão pegar.

Primeiro, você precisa diminuir a velocidade do peixe. Na verdade, é bem fácil, você só precisa esperar um pouco depois de mover esses 10 passos. Há um bloco **Controle ** que irá ajudá-lo aqui:

```blocks3
    wait (1) secs
```

\--- task \---

Adicione o bloco `espere`{:class="block3control"} no seu código dentro do bloco `sempre`{:class="block3control"}, e altere o número para `0.5`, assim:

```blocks3
    when green flag clicked
    forever
        move (10) steps
+      wait (0.5) secs
    end
```

\--- /task \---

## \--- collapse \---

## title: Fazendo ajustes

O número que você define no bloco `espere`{:class="block3control"} diz quantos **segundos** você quer que o peixe espere. `0.5` é meio segundo.

Você pode testar diferentes valores para ver qual é o melhor para o jogo. E lembre-se que você pode mudar o número de passos dentro do bloco `mova`{:class="block3motion"} também!

\--- /collapse \---

O peixe se move agora, mas você também precisa que ele volte quando chegar na borda do Palco. Mais uma vez, há um bloco **Movimento** para isso!

\--- task \---

Encontre o bloco `se tocar na borda, volte`{:class="block3motion"} e adicione-o após o bloco `espere`{:class="block3control"}.

\--- /task \---

## \--- collapse \---

## title: O que o novo bloco faz?

O bloco `se tocar na borda, volte`{:class="block3motion"} verifica se o ator está tocando a borda do palco e, se assim for, vira para a esquerda, para a direita, para cima ou para baixo conforme o caso.

\--- /collapse \---

Obviamente, isso levará a um peixe de cabeça para baixo, então você precisa de um bloco `defina o estilo de rotação para`{:class="block3motion"} novamente.

\--- task \---

Atualize seu código para definir o estilo de rotação dos peixes como `esquerda-direita`{:class="block3motion"} no início do script do ator:

```blocks3
    when green flag clicked
+    set rotation style [left-right v]
    forever
        move (10) steps
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

O peixe se move para trás e para frente agora, mas apenas em uma linha reta — um pouco fácil demais para o jogador pegar com o tubarão! Você precisa tornar o peixe menos previsível.

Você já sabe de um passo anterior como fazer um ator girar, então comece por aí.

\--- task \---

Adicione um bloco gire nas instruções do ator peixe e clique na bandeira verde.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever
        move (10) steps
+        turn cw (10) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

É melhor, mas o peixe ainda se move dentro de um padrão. Precisa ser mais aleatório. Felizmente, o Scratch pode ser aleatório para você! Você só precisará de um novo tipo de bloco, chamado bloco **Operador**.

## \--- collapse \---

## title: O que é um operador?

**Operadores** pegam um ou mais valores (como números, texto, ou `Verdadeiro/Falso`) e retornam um único valor. Você pode dizer o tipo de valor que ele retornará pela forma do bloco: as extremidades redondas dão números ou textos, as extremidades pontudas dão `Verdadeiro/Falso`.

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Encontre o bloco `número aleatório entre`{:class="block3operators"} na categoria **Operadores**, e conecte-o ao bloco `gire _ graus`{:class="block3motion"} da categoria **Movimento**, clicando nele e arrastando-o para o campo onde você define o número de graus.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
+        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

**Nota**: você pode alterar os números mínimos e máximos que ele escolherá, mas os valores padrão (`1` e `10`) são muito bons para este jogo, então você pode deixá-los.

\--- task \---

Clique na bandeira verde para executar o código!

\--- /task \---

## \--- collapse \---

## title: Então, o que faz o bloco sempre?

O bloco sempre agora faz o ator peixe fazer quatro coisas nesta ordem:

1. Mover para frente
2. Girar um pouco
3. Esperar brevemente
4. Verificar se está na borda do palco

Depois que o ator fizer a verificação, ele começará novamente no início do loop e se moverá, girará, esperará, verificará enquanto você deixar o programa Scratch em execução.

\--- /collapse \---

Legal! Em seguida: pegar aquele peixe!