#keylog

A simple keylogger for Linux written in C. Currently requires your keyboard input event file to be `/dev/input/by-path/platform-i8042-serio-0-event-kbd`.

## Usage

```bash
cd keylog/
sudo ./keylog -f "file-to-write-to.txt"
```

This will log all keystrokes to the specified file while the program is running.

## Output Format

Each key press will cause a string representing that key to be written to the
chosen location, followed by a newline. When the program quits, an extra newline will be added.

#### Example

Typing `hello world` and then quitting the program with `Ctrl-C` will cause the chosen location to contain the following.

```
H 
 E 
 L 
 L 
 O 
 SPACE 
 W 
 O 
 R 
 L 
 D 
 LEFTCTRL 
 C 


```

## Building

```bash
cd keylog/
make
```
