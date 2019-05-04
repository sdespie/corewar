# Corewar

Corewar is a 19 Coding School project. The purpose of this project is an implementation of the programming game **“Core War”**.

# What is Corewar?

• Corewar is a very peculiar game. It’s about bringing “players” together around a
“virtual machine”, which will load some “champions” who will fight against one another
with the support of “processes”, with the objective being for these champions
to stay “alive”.


• The processes are executed sequentially within the same virtual machine and memory
space. They can therefore, among other things, write and rewrite on top of
each others so to corrupt one another, force the others to execute instructions that
can damage them, try to rewrite on the go the coding equivalent of a Côtes du
Rhône 1982 (that is one delicious French wine!), etc...


• The game ends when all the processes are dead. The winner is the last player
reported to be “alive”.


__Wikipedia ("Core War"):__ https://en.wikipedia.org/wiki/Core_War

![Corewar](/resources/corewar.svg)

[corewar.en.pdf](/resources/corewar.en.pdf) is the task file.

# Authors

**Sebastien De Spiegeleer**: Team Lead, VM (workflow, visualisation, parsing), Champion

**Charles-Antoine Van Beers**: VM (workflow, operations)

**William Brakckman**: ASM compilator (finite automaton lexer + parser + translator)

**Nathan Rouvroy**: Online Game (server, client)

# Breakdown of the project’s objectives


This project can be broken down into __three distinctive parts__:


• __The assembler__: this is the program that will compile your champions and translate
them from the language you will write them in (assembly language) into “Bytecode”.Bytecode
is a machine code, which will be directly interpreted by the virtual
machine.


• __The virtual machine__: It’s the “arena” in which your champions will be executed.
It offers various functions, all of which will be useful for the battle of the champions.
Obviously, the virtual machine should allow for numerous simultaneous processes;
we are asking you for a gladiator fight, not a one-man show simulator.


• __The champion__: This one is a special case. Later, in the championship, you will
need to render a super powerful champion, who will scare the staff team to death.
However, rendering this kind of champion is serious work. And since, for now, we
are mostly interested in your capacity to create Corewar’s other programs (i.e. the
assembler and virtual machine), your current champion will only need to prove to
us that you can write bits and pieces of Corewar ASM. This means that the champion
you should render for this project only needs to scare the bejesus out of a
neurasthenic hedgehog.

# Project Structure

This project consists of five parts:

* Champion
* Assembler
* Virtual Machine
* Online Game (Bonus)
* Visualizer (Bonus)

Project has one developed champion: `pod.s`. It is located at the [`root` directory](/).

Assembler is the program `asm`.

Virtual Machine + Visualizer are modules of the program `corewar`.

Online game is combined by server and client programs.

# How to clone?

If you want to clone it, you can use the following command:

```
git clone https://github.com/sdespie/corewar.git
```

# Installation

Clone repository and then go into the created directory and run the following command:

```
make
```
Tested on OS X 10.11. Requires ncurses to be installed.

## Usage

### `asm`

```
Usage: ./asm (champion.s)
```

### `corewar`

```
Usage: ./corewar [-dump nbr_cycles] [-visu] [-sounds] [[-n number] champion1.cor ...]

	  -dump nbr_cycles:
	          Dumps memory after nbr_cycles then exits.
	  -visu           :
	          Use the visual mode to display the battle, live.
	  -sounds         :
            Use sounds mode to add special effect to the battle.
	  -n number       :
	          Set the number of the following champion to number.
```

### `Online Game`

```
Usage server: ./server
Usage client: ./online [IP SERVER] [Champion.cor]
```

## Visualizer

The best visualizer performance is with **iTerm2**.

![Visualizer](/resources/visu0.png)

![Visualizer](/resources/visu.png.png)

![Visualizer](/resources/core1.gif)

![Visualizer](/resources/core2.gif)
