Flex container 
display : - flex - элементы распологаются как строчные но не всю ширину контейнера 
          - inline - flex  элементы распологаются как строчные **всю** ширину контейнера 
Свойства для контайнера : 
- flex direction - направление главной горизонтальной оси 
- flex wrap - Перенос элементов и отступы
- flex flow 
- gap
- justify content
- align items
- align content 
Свойства для элемента: 
- align self 
- flex grow 
- flex shrink
- flex basic
- flex
- order 
# Направление осей flex direction   
Свойства: 
- row (default) горизонтально по порядку 
- row - reverse горизонтально в обратном направлениее 
- column - по вертикали или в колонку блочный тип 
- column reverse - по вертикали или в колонку блочный тип в обратном направлении 


# Перенос элементов и отступы flex wrap 
Свойства:
- wrap - позволяет переносить элементы на новую строки при заданном разрешении 
- wrap reverse - тоже самое но наоборот 


# Выравнивание вдоль главной оси
Для контейнера исвольем 3 свойства 
- justify-content - выравнивание по по горизантали (главной оси ) свойства :

1)flex start смещает элементы к началу 
2)flex end смещает элементы к концу 
3)center по центру 
4)space-between  равномерно распределяет элементы первый и последний элемент приэаты к краям
5)space around  равномерно распределяет (крайнии элементы имееют рахный отступ от )
6)space evenly  равномерно распределяет элементы (везде отступы одинаковые)

- alignt-items - выравнивание по вертикали 
-  align-content - для вырванивание элементов расположенныъ в несколько строк 

**Если элементы представлены в блочной модели через flex-direction: column и им не задана высоту через height , то элементы выравнивать не будут  !!!**

Для элементов 1 свойство 
- align-self- для индивидуального выравниваие элемента 

# Выравнивание вдоль поперечной оси align-items по вертикали 
**Если элементы представлены в блочной модели через flex-direction: column и им не задана высоту через height , то элементы выравнивать не будут  !!!**
- align-items  свойства 
1)flex start смещает элементы к началу 
2)flex end смещает элементы к концу 
3)center по центру 
4)baseline 

#  Многострочное выравнивание (Alignment: align-content) вырвавнивает по вертикали 
Работает только при свойстве flex-wrap : wrap 
align-content: stretch  
flex start смещает элементы к верху выравнивание по вертикали 
flex end смещает элементы к низу выравнивание по вертикали 
center - центр по вертикали 
space-betmeen - расстроягние между ними 
space around  равномерно распределяет между бакраунд 

# Индивидуальное выравнивание элементов (Alignment: align-self)
Вырвавнивае определенного элемента будет по вертикальной оси. Работает только если задана height для контейнера


#  Размеры элементов (Flexbox Sizing)
- flex-grow используется для задания пропорции свободного пространства , чем **больше** число тем больше места занимает элемент места. Позволяет убрать отступы от бордера 

- flex-shrink используется для задания пропорции свободного пространства на сколько много пространство готов отдать элемент , чем **меньше** число тем больше места занимает элемент места 

- flex basic опеределяет размер элемента до распределения свободного пространства , при горизонтальном устанваливает ширину , при вертикаольном выосту 

# Определение порядка элементов (Order) 
Определяет распределение элементов по оси изнчально задан 0 
order - 0 
определение порядка схожу с числовой осью 
-2 - 1 0 +1 +2 соответсвенно присваевая знчаение большее от нуля будет распологать элемент правее , меньшее от нуля левее 

