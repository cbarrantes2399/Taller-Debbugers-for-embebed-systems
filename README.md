Notas:

- Montar mapa conceptual para delimitar tema
- Buscar sobre depuradores en la página de Yocto
- Definir cuáles son los más comunes y si se instalan fácil o no, y si son fáciles de usar
- La estructura puede ser algo como:
  - Errores comunes
  - Tal vez hablar entre la diferencia entre debuggers de código y de sistemas embebidos
  - Lista de depuradores
  - Explicación de los más comunes

- Para tutorial, tal vez cocinar una imagen de Yocto ya con un depurador listo

de Emulators and Debuggers.pdf

Debugger:
Tool to test and debug other programs.
Can find failures and causes.
2 types:
  - Source Level
    Can show positions in code.
  - Low Level
    Can show lines in program.

Embedded debugger usually has 2 parts:
- Kernel (target)
- host that communicates with kernel and database and symbol tables

Requirements for debugger:
- start, stop, peek, poke processor and memory
- mem substitution ROM for RAM for rapid download, debug, repair cycles
- be able to analyze execution in real time

Kernel should be nonintrusive:
- run as a separate process and only execute during breakpoints.

Types of debuggers:
  - simulators
  - in circuit emulators
  - remote target processors

Simulator:
  host based program, simulates functionality and isa
  front end has text of GUI for source code, registres, etc.
  valuable in early stages
  disadvantage: processor, but not peripherals

  ¿what are some simulators?

Remote debuggers:
  monitor/control embedded SW. Download, execute, debug software over communication link.
  (front end) Program on host has GUI just like any other debugger. Either shell or GUI.
  (back end) Low-Level control of target processor, runs on target, communicates to front-end over com. link
  Since program being debugged runs on different HW than debugger, lots of interaction:
  - start restart kill step
  - software breakpoints