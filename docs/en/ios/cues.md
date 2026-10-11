# Cues (iOS)

The **Cues** tab shows the cue list live from the console and highlights the cue that is currently running. You can see where the show stands right on your phone.

## Requirement

The app must be connected to EOS (see [OSC](./osc)). A status bar at the top shows the connection state. Without a connection the list stays empty.

## List

Each row shows the cue number and name. The active cue is highlighted in green with a play icon, the next cue carries an orange icon. When the active cue changes on the console, the list scrolls to it automatically.

Changes on the console — a new, renamed or deleted cue — appear on their own. The list does not poll; the console reports every change.

## Multiple cue lists

If the console has more than one cue list, a dropdown for choosing the list appears at the top left. With a single list it is hidden.
