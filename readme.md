#garbage
Репозитарий (repo), содержание которого соответствует названию!

... библиотеки:
1. data
- не самая полезная вещь, содержит модели DataModel, но их всеравно надо править и они не отрабатывают fireDataChenged/
- лучше модели каждый раз писать заново, не на столько сложно, зато можно функционал модели под задачу определить.
 <dependency>
      <groupId>esoe</groupId>
      <artifactId>data</artifactId>
      <version>0.1-SNAPSHOT</version>
</dependency>

2. loger
- буду тестить что получилось и дорабатывать.
- loger предназначен для мониторинга хода выполнения программы, основное использование в ходе отладки программы.
- метод использования:
             >>>>>>> СМОТРИ ВНУТРИ <<<<<<<<<<
             
             1. Для подключения к проекту, достаточно объявить переменную класса Loger:
             Loger log = new Loger(); //после этого можно начинать коментировать лог
             
             2. чтобы просматривать лог сообщений, установленных разработчиком по ходу выполнения программы,
             нужно инициировать WidgetLoger:
             new WidgetLoger().initFrame();//чтобы открыть в самостоятельном окне можно log.initWidget();
             или добавить панель WidgetLoger на свою форму.
             
             3. По умолчанию виджет содержит два лога: DEFAULT и USER, можно добавить еще логи при необходимости:
             ModelListener modelUSERlistener;
             log.addModel("USER");//модель USER добавлена в loger
             modelUSERlistener = new ModelListener(log.getModel("USER"), ta);//слушатель USER
             log.getModel("USER").addTableModelListener(modelUSERlistener);
             
             4. Пример обращения:
             log.getModel("USER").message("... выбрана модель ..." + modelChoice + " ...");
             
<dependency>
      <groupId>esoe</groupId>
      <artifactId>loger</artifactId>
      <version>0.1-SNAPSHOT</version>
</dependency>
