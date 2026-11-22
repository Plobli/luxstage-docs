# Cues (iOS)

The **Cues** tab shows the cue list live from the console and highlights the cue that is currently running. The playback buttons sit right below it. You run the show and jump to any cue without switching views.

## Requirement

The app must be connected to EOS (see [OSC](./osc)). At the top left you pick the stage, with the connection state right below it. Without a connection the list stays empty and the buttons are greyed out.

## List

Each row shows the cue number and name. The active cue is highlighted in green with a play icon, the next cue has an orange background. When the active cue changes on the console, the list scrolls to it automatically.

Changes on the console — a new, renamed or deleted cue — appear on their own. The list does not poll; the console reports every change.

## Jumping to a cue

Tap a cue. It turns purple and **Go to Cue X** appears below the list. Only this second tap triggers the jump on the console, so you don't jump by accident during a performance. **Cancel** or tapping the same cue again clears the selection.

## Playback buttons

| Button | Colour | Function |
|--------|--------|----------|
| **Stop/Back** | Orange | Tap once to stop the running cue, tap twice to go back to the previous cue (like the Stop/Back key on the console) |
| **GO** | Green | Start next cue |
| **Go Time Disable** | Teal | GO without cue time (Shift+GO) |
| **Cue Out** | Red | Jump directly to Cue Out |
| **Cue** | Purple | Enter a cue number on a keypad and jump to it |

## Multiple cue lists

If the console has more than one cue list, a dropdown for choosing the list appears at the top right, next to the title. With a single list it is hidden. With several lists, all buttons (GO, Stop/Back, Go Time Disable, Cue Out) and jumps act on the selected list. With a single list, the buttons control the main playback, just like on the console.
