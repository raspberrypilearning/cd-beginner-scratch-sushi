## Pescando!

O tubarão se move, o peixe nada, mas eles não interagem: se o peixe nada na boca do tubarão, nada acontece. Hora de mudar isso!

Primeiro, você precisa saber se o peixe está tocando o tubarão. Para isso, você precisará de um bloco **Controle** e de um bloco **Sensores**.

--- task ---

Adicione o bloco `se...então`{:class="block3control"} da categoria **Controle** dentro do loop `sempre`{:class="block3control"} do ator peixe, abaixo do bloco `se tocar na borda, volte`{:class="block3motion"}.

Arraste o bloco `tocando em ...`{:class="block3sensing"} para o espaço no topo do bloco `se...então`{:class="block3control"} e clique no triângulo pequeno para selecionar o nome do ator tubarão. Se não alterou, será "Sprite1".

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: Como isso funciona?
---

O bloco `se...então`{:class="block3control"} da categoria **Controle** precisa receber um valor `Verdadeiro/Falso`.

Blocos **Sensores** coletam informações, como onde está o ator, o que está tocando, etc. Você está usando este bloco:

```blocks3
    <touching [Sprite1 v] ?>
```

Das extremidades pontiagudas deste bloco, você pode dizer que ele lhe dará o valor `Verdadeiro/Falso` que o bloco `se...então`{:class="block3control"} precisa.

--- /collapse ---

Claro, você acabou de adicionar um bloco `se...então`{:class="block3control"} sem adicionar nada para a parte 'então'. Então, no momento, o seu programa está verificando se o ator peixe está tocando o ator tubarão, mas não está fazendo nada acontecer em resposta.

Você pode fazer o peixe desaparecer, como se o tubarão o comesse, usando o bloco `esconda`{:class="block3looks"}.

--- task ---

Encontre o bloco `esconda`{:class="block3looks"} na lista **Aparência**, e coloque-o dentro do bloco `se...então`{:class="block3control"}, assim:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

Agora, uma vez que o tubarão pega o peixe, o peixe desaparece para sempre. Isso não é bom.

--- task ---

Coloque o bloco `mostre`{:class="block3looks"} de **Aparência** no início do código do peixe, para que você possa reiniciar o jogo.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

Isso já é melhor, mas você não quer que o jogador reinicie o jogo toda vez que pegar um único peixe!

--- task ---

Atualize o código dentro do seu bloco `se...então`{:class="block3control"} para ficar assim:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: Como isso funciona?
---

Você está sendo esperto aqui: quando o peixe está escondido, ele espera, se move e depois aparece novamente.

Parece que muitos peixes continuam aparecendo, mas é esse ator se movendo!

--- /collapse ---

Isso é um jogo! Mas ainda não há como manter a pontuação ou vencer. Você também pode corrigir isso — no próximo cartão!