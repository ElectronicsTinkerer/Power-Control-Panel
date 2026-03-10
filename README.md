# Custom Remote-Controlled Power Distribution Panel

**Insert cool, complete build picture here ;)**

## On PCB versioning

Each PCB has a version number in the format of `1.0A`. The basic format comes down to this:

```
1.   - Major design revision. Full re-architect of the board with maybe a subsystem or two copied over.
  0  - Minor schematic revision. Something that affects few components or connections.
   A - Layout revision. For a given Major.Minor combination, this is the layout iteration number.
```

This version ID is frozen at time of order. This means that until someone clicks the "order design" button at the fab house, the above numbering system does not update. Since it is not uncommon to have more than one export operation when generating gerbers, when generating fabrication outputs, a number, starting at `0` is appended to the above version and maintained on the fabrication output archive. Each export operation increments this number. For example, if a board is exported and upon inspection of the gerbers, it is discovered that the drill file is missing or the file format is incorrect, the gerbers are re-exported and this fabrication ID is incremented. This ensures that the fabrication output version which is ordered can be identified by looking for the highest export ID for a given Major.Minor.Layout version.

In case you're wondering, I have no idea where this scheme came from. I've been using it on boards for probably a decade :)
