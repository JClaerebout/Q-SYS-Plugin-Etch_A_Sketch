# Etch A Sketch 1.0.0

A two-knob drawing toy for Q-SYS, rendered as dynamic SVG. The drawing and toy artwork are generated inside [Etch_A_Sketch.qplug](Etch_A_Sketch.qplug); no separate image files or external services are needed.

## Install and draw

1. Double-click `Etch_A_Sketch.qplug`. QSysPluginHelper will prompt you to install the plugin.
2. Add **Games > Etch A Sketch** to a design and start emulation or run the design on a Core.
3. Open the component and turn **Horizontal** and **Vertical** to draw. Both knobs range from 0 to 100; drawing starts at the center.

## Controls

- `Horizontal` moves the pen left or right; `Vertical` moves it down or up.
- `PenUp` lets you move without drawing. Turn it off to resume drawing.
- `Clear` erases the drawing and returns both position knobs to the center.
- `LineWidth` sets the width of the whole drawing from 1 to 8, with a default of 3.
- `SegmentCount` shows the number of stored line segments. The drawing retains the latest 1,500 segments, removing the oldest as new ones are added.
- `Display` shows the SVG drawing. Drawings are held in memory and reset when the runtime restarts.

## UCI integration

Copy `Display` and the drawing controls from the component into a UCI. Keep the display at its original 610:407 aspect ratio. Position, pen, and line-width controls expose input and output pins; `Clear` exposes an input pin and `SegmentCount` an output pin. The display is UI-only.

## License

[MIT](LICENSE). Copyright (c) 2026 Jens Claerebout.
