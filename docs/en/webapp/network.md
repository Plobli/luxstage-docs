# Network

The **Network** tab documents a venue's IT infrastructure — network outlets, devices, switches and their cabling — independent of shows and venue templates.

## Elements

An element is one of the three building blocks of the network documentation:

| Type | Meaning |
|------|---------|
| **Outlet** | A network outlet (wall/floor connection point) |
| **Device** | An end device (e.g. access point, camera, PC) |
| **Switch** | A network switch with a fixed number of ports |

Elements are created via the **"+ Add element"** button below the elements table (choose the type). Each element has:

- **Type** — Outlet, Device or Switch (changeable via dropdown)
- **Label** — free-text name
- **Location** — assign to a room or leave as "No location"
- **Ports** (switches only) — number of switch ports
- **Main switch** (switches only) — checkbox to mark a central switch; multiple switches can be marked as main switch at the same time

An element is removed via the trash icon in its row. If connections still exist for that element, a dialog warns that they will be removed as well.

## Locations

Elements can be assigned to a **location** (room) — the elements table automatically groups by location, showing the number of elements per group. Each group can be collapsed and expanded by clicking its header. Elements without a location appear in the "No location" group.

A new location is created directly in an element's location dropdown via **"+ New location…"**.

## Search

The search field at the top right of the elements table filters the list in real time.

## Connections

Connections represent the cabling between two elements.

### Switches as a port grid

For each switch, the view shows a grid with one field per port (matching the configured port count). Each port shows:

- A dropdown to choose which element is connected to that port (or "Empty")
- An additional port field if the other end is also a switch — so the connection between two switches can be traced on the port level from both sides

Above each grid, a badge shows utilization, e.g. "(6/24)". Switches without a configured port count show "No port count set." instead.

### Other connections

Connections that don't involve a switch (e.g. device directly to device) additionally appear in their own table with "From", "To" and a third column with a trash icon to delete the connection. New connections are created via **"+ Add connection"**; as long as both ends aren't chosen yet, the entry stays a draft (highlighted) and is only saved once the selection is complete.

::: tip Only valid combinations are selectable
When assigning a connection partner, only elements that make sense to connect given their element type are offered. If a target has already reached the maximum number of connections, a dialog asks whether to replace the oldest one.
:::

## Topology (interactive graph)

Above the elements and connections tables, the topology view shows all elements as freely movable nodes, connected by lines (cables) according to the configured connections.

- **Draw a connection** — drag directly in the graph from one connection point to another to create a new connection
- **Reconnect** — grab an existing line at its endpoint and drag it onto another element
- **Delete an element/connection** — select it and press Delete/Backspace
- **Auto-arrange** — automatically arranges new, not-yet-placed elements (switches as the starting point); elements moved manually keep their position
- **Save / restore view** — save the current node layout, or reset to the last saved state
- **Fullscreen** — display the topology canvas in fullscreen mode (also exit via Esc)

If no elements have been created yet, the topology shows "No elements yet."

## Live collaboration

As with shows, the network documentation locks as soon as another person is actively editing — a notice shows who is currently holding the lock.

## Undo / Redo

Changes to elements and connections can be undone and redone via the buttons at the top right (or the usual keyboard shortcuts).

## PDF export

The **"Export PDF"** button at the top right downloads the complete network documentation as a PDF.
