# Использование include и import
## даёт возможность в одном плейбуке использовать другие плейбуки

### Можно просто писать: 
             tasks:
             - include_tasks: create_files.yml 

             
### Можно добавлять своё значение  в переменные при вызове инклуд (они могут быть определены по умолчанию, а мы присваиваем им своё значение):
              vars:
                mytext: "Privet ot ST"
              tasks:
              - include_tasks: create_files.yml 
                vars:
                  mytext="Hello, this is our variable value"
  
  
## Отличие include и import:
## include - 
ансибл проходит по плейбуку и запускает его, но контент импортированных файлов и значения переменных 
подставляются только, когда выполнение доходит до инклуд.

## import - 
после запуска ансибл проходит по плейбуку и сразу же вставляет контент импортированных файлов (других плейбуков),
и сразу же подставляет значения в переменные.


  
