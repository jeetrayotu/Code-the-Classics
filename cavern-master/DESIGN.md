# Screens Architecture

Screens for playing, the menu, and game over events have been
implemented by creating subclasses inheriting from `pgzero.screen.Screen`.
They are updated and drawn from the `App` instance using a `getattr`
call with the instance and the current input state passed in.

# Input Design

Keypresses are now registered from the individual screens'
`update` functions. The `Player` class now uses an instance of an
`InputState` dataclass to execute character actions.

# How Pause Works

It does not.