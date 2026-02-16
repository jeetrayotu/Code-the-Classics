# Cavern Master
## How to Run the Game

```bash
python ./cavern-master/cavern.py
```

## Architectural Changes

As detailed in the commit messages:
* A [`uv`](https://docs.astral.sh/uv/) project has been initialized.
* `state` now uses a string instead of `ENUM` values,
simplifying the `app.update` and `app.draw` functions.
* `app.update` and `app.draw` have been split up between the `App` class and various `Screen` subclasses.
* An `InputState` dataclass has been created and initialized,
allowing for the refactoring and removal of the global `space_down`
function.
* Edge detection has potentially been implemented.