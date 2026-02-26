**PQM**

Проект, который представляет из себя программируемый модуль управления параметрами генерации зондирующего сигнала. 
Мнемоники для управления записываются в BRAM, откуда вычитваются и исполняются. Это позволяет изменять конфигурацию параметров генерации сигналов, не изменяя RTL.
## Доступные мнемоники:

```
GEW - gpio external write (регистр пробрасывается в модули верхнего уровня) 
GES - gpio external set 
GER - gpio external reset 
GIW - gpio internal write (управление периферией ядра PQM) 
GIS - gpio internal set 
GIR - gpio internal reset 
SAMP - set amplitude (установка амплитуды перед ЦАП) 
SZFC - set zero frequency carrier (установка начальных значений частот для генерации гармонической заполняющей) 
SZFR - set zero frequency rotator 
SFIC - set frequency increment carrier (установка значений инкремента частоты сигнала для формирования ЛЧМ заполняющей) 
SFIR - set frequency increment rotator 
SPC - set phase carrier (установка начальных фаз) 
SPR - set phase rotator 
JMP - jump to label 
AJMP - absolute jmp 
NOP - no of operations 
SMOD - set modulation mode (TODO: удалить для оптимизации дешифратора до 4 обрабатываемых бит на команду)

```

Формирование содержимого BRAM с мнемониками можно осуществить с помощью этих исходников:
https://github.com/FernandesKA/PQM_cmd_to_coe
