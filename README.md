# STM8S-UART-DebugTool

Утилита DebugTool предназначена для чтения и записи регистров МК через UART в проекте STM8S-UART-DebugDev.

Среда разработки и компилятор - Microsoft Visual Studio 2015 + Windows Driver Kit 10

Использование:

DebugTool.exe l/list/read/r/write/w width(8/16bit) register_addr register_data


Список COM портов: DebugTool.exe list

Пример:

=========================================

: DebugTool.exe list

1 COM port(s) available.

List:

COM3

=========================================


Чтение регистра: DebugTool.exe read COM_port_name width register_addr

Пример:

=========================================

: DebugTool.exe read COM3 8 0x5007

Reading register 0x5007 (8 bit) using COM3... OK!

Register addr: 0x5007

Width: 8 bit

Register data: 0x0

=========================================

Запись регистра: DebugTool.exe write COM_port_name width register_addr register_data

Пример:

=========================================

: DebugTool.exe write COM3 8 0x5007 0x20

Register addr: 0x5007

Width: 8 bit

Register data: 0x20

Writing register using COM3... OK!

=========================================
