# Pomodoro Timer

This Bash [Pomodoro Timer](https://www.pomodorotechnique.com/what-is-the-pomodoro-technique.php)
is a simple command-line tool to help users implement the Pomodoro Technique, a
time management method that uses a timer to break down work into intervals,
separated by short breaks.

![demo img](https://github.com/marcoplaitano/images/blob/main/pomodoro.png)

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## Usage

1. Clone the repository and make the script executable:

```sh
git clone https://github.com/marcoplaitano/pomodoro-bash
cd pomodoro-bash
chmod +x pomodoro.sh
```

2. Run the pomodoro timer:

```sh
./pomodoro.sh
```

By default, it alternates between *Focus* slices of **25** minutes and *Pauses*
of **5**.  
After **3** iterations, a *Long Pause* of **20** minutes is earned.

The timer can be controlled with case-**in**sensitive key presses:

+ `P` to pause or resume
+ `N` to skip to the next slice
+ `Q` to quit the script

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## Configuration

Open the `pomodoro.sh` file to edit the following variables:

+ **TIMES**  
    Duration (in minutes) of each slice
    ```sh
    declare -A TIMES=(
        [FOCUS]=25
        [PAUSE]=5
        [LONG PAUSE]=20
    )
    ```

+ **NUM_ITERATIONS**  
    Number of *Focus* slices to complete before a *Long Pause* is earned
    ```sh
    NUM_ITERATIONS=3
    ```

+ **SOUNDS**  
    Sounds to play when notifying the beginning of a new slice
    ```sh
    declare -A SOUNDS=(
        [FOCUS]="/usr/share/sounds/focus.oga"
        [PAUSE]="/usr/share/sounds/pause.oga"
        [LONG PAUSE]="/usr/share/sounds/pause.oga"
    )
    ```

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## Author

Marco Plaitano

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## License

Distributed under the [MIT](LICENSE) license.

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## Acknowledgments

Pomodoro Technique: https://www.pomodorotechnique.com/what-is-the-pomodoro-technique.php
