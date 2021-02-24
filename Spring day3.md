Конфигурация с помощью аннотаций
XML
   <context:component-scan base-package="ati packagedn"/>
   
@Component("catBean")--->id bean
public class Cat{
}

esli id bean jazbasa classtyn aty id bolady kiwi arippen,esli bastapki eki arip ulken bolsa onda auispaidi
  Процесс внедрения зависимостей при использовании @Autowired такой:
     1. Сканирование пакета, поиск классов с аннотацией @Component
     2. При наличии аннотации @Autowired начинается поиск подходящего по типу бина
     Далее ситуация развивается по одному из сценариев:
      *Если находится 1 подходящий бин, происходит внедрение зависимости;
      *Если подходящих по типу бинов нет, то выбрасывается исключение;
      *Если подходящих по типу бинов больше одного, тоже выбрасывается исключение
 prosto ustine(constructor,setter) @Autowired dep jaza salu
 
 Типы autowiring-а или где мы можем использовать данный DI:
    •Конструктор
    •Сеттер
    •Поле
