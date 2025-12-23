Trying to replicate tiny open hand [CodeActAgent](https://github.com/All-Hands-AI/OpenHands.git)

## What is this?

It's my attempt at reproducing OpenHand's CodeActAgent or you could also say codex or claude code agent. It throws away all the complexity such as Controller, EventStream, Runtime UIs and many other thing, keeping only what's cruical to the CodeActAgent.

It uses bash terminal, terminal commands, create a new file, write to a new file, edit the file at specific lines, all autonomously based on the instruction provided by the user.

Here's a simple lightweight example video.

[![Watch the video](https://img.youtube.com/vi/8bN6JtvXUrk/maxresdefault.jpg)](https://youtu.be/8bN6JtvXUrk)

I prompt the agent to write me a script to simulate solar system in javascript. It first.

1. searches what exisitng files there are on folder by calling bash tool
   `ls -la /Users/cohlem/Projects/Experimentation/TinyOH"}`

2. Takes the output of the `ls` command as new input and generate the solar system code.

3. Saves the code to `solar_system.html` file at directory `/Users/cohlem/Projects/Experimentation/TinyOH`

4. I prompt the agent it make it look like 2.5D.

5. It reads the existing `solar_system.html` file.

6. Generates only the necessary code to convert it from 2D to 2.5D

7. Calls tool to replace only the spcific part of the code.

## How do i run this project?

Just run the following command, it will ask for your instructions, enter it and see what it does with it.

```python
python -m TinyOH.main
```
