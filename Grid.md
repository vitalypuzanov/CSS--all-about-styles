# Display grid

    display:grid 
    grid-template-columns: 100px, 1fr, 200px 

![grid](./g1.png) 

<b> Fr - фактор гипции , коэфециент пропорциональности, отталкиеваться от общего колва фракций <b>


## Grid-template-columns 
<b> grid-template-columns - центрирует наши элементы по горизантали делая их строчными, а в свойствах мы записываем размер элементов <b>

Фракции работают как дроби если у нас есть:

      grid-template-columns: 1fr 2 fr 3fr  

<b> Это эквивалентно 1\6, 2\6, 3\6 <b>

![grid](./g2.png) 

Параметры :
- px
- em
- %
- FR
- min-content
- max-content - подстаривается под ширину контента при этом создавая ползунок прокрутки, если контент слищком большой 
- minmax(min,max) - позволяет задавть гибкую ширину колонки через параметры 
- repeat(n, s ) n- кол-во элементов , s - их размер

## Grid-column-gap

      Grid-column-gap - свойства задет ширину между колонками 

# Управление размерами и позицией grid-элемент 

Свойства: 

    grid-column-start; 3 - начало по ширине 
    grid-column-end 4 - конец по ширине 
    grid-row-start; 3 - начало по высоте
    grid-row-end 4 - конец по высоте 

![grid](./g3.png)

Можно сократить эти свойства и будет тоже самое:

      grid-column 3/4
      grid-row 3/4 

![grid](./g3.png)

Можно сохратить еще больше: 

      grid-area: 1/3/4/4 

(1/3 - это grid-column 1/3, 4/4 - это grid-row 4/4)

![grid](./g4.png)


**Для простоты запоминая**

 ![grid](./g5.png)


      
##  Именование grid-линий, создание сетки

      grid-template-columns: repeat (12 [col] fr)
12- Кол-во элементов, [название колонки], размер в нашем случае fr


      grid-template-row: repeat (12 [row] fr)
12- Кол-во элементов, [название колонки], размер в нашем случае fr

## Центрирование контента

Для родителя 

      .grid {
        display: grid
        grid-template-column:1 fr
        grid-template-row:1 fr
        align-item: center, start, end, stretch
        justefy-item:center, start, end, stretch
      }

Для элемента 

      .grid-item1{
        align-self: stretch , end , start, center
        оustefi-self: stretch , end , start, center
      }

Align-self - выравниваение по вертикали :
- stretch
![grid](./g6.png)
- end
![grid](./g7.png)
- start
![grid](./g8.png)
- center
![grid](./g9.png)


Justefi-self - выравниваение по горизонтали :
- stretch
- end
![grid](./g10.png)
- start
![grid](./g11.png)
- center
![grid](./g12.png)


## Выравнивание контента 

Выравнивание в контейнере иммет такие же свойтсва как и flex 

     justfi content: start ,end ,center ,space-around, space-betwenn, space, space-evnly 
     align content: start ,end ,center ,space-around, space-betwenn, space, space-evnly 


## Управлять порядком элементов внутри grid-контейнера 

Как fkex direction

    Grid auto-flow: row, column Dense

Dense - позволяет при разных размерах не оставлять пустого пространства.

<b>ДО<b>

![grid](./g13.png)

<b>После<b>

![grid](./g14.png)

Свойство order задает порядок 

    order: -1 

![grid](./g15.png)

