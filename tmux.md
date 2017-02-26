# tmux Cheatsheet

## Concepts
tmux can be thought of as a window manager (terminal multiplexer) for the terminal. The following building blocks are nested to create the final picture, each with a one-to-many relationship:

    Server > Session > Window > Pane
    
If you compare tmux to a skyscraper:

    Server    Foundation    - you only need one
    Session   Floor level   - you need at least one for the building to work
    Window    Apartment     - separate from other apartments on the same floor
    Pane      Room          - each room has a specific purpose, kitchen, living room => command line

### Server
The tmux server is the foundation on which the other blocks are built. This server is the reason that sessions can be persisted for a long time. In practice you don't need to explicitly interact with tmux server instances directly.

### Sessions
You must have at least one session to use tmux. The session is what you connect to which holds your windows and panes. The session name is the first entry from the left in your status bar (by default).

### Window
A window is what fills your screen at any point in time. Windows have names and an index number. The active window is highlighted with a * in the status bar.

### Pane
One or more panes fill a window. Each pane can run its own command. A pane is what you would usually only have one of with a standard ssh connection.

## Commands
