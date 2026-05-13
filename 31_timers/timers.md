Go timers are modeled with `sleep`. Timer 1 fires after 2 seconds. Timer 2 is stopped before it fires, so only "Timer 2 stopped" is printed; the second 2-second sleep confirms it never fires.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The first timer will fire ~2s after we start the program, but the second should be stopped before it has a chance to fire.
___
##### Run Command:

`$ zig run -lc timers.c`

##### Results:

`Timer 1 fired`
`Timer 2 stopped`
