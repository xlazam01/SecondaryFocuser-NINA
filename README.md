# Secondary Focuser — N.I.N.A. plugin

Autofocus for the **guide camera** (OAG camera or guide-scope camera) with a **second focuser**, while
N.I.N.A. keeps driving the main focuser of the imaging train.

| Focuser | Moves | Driven by |
|---|---|---|
| Main focuser | whole imaging train: main camera, filters, OAG | N.I.N.A. (built-in autofocus, filter offsets) |
| Secondary focuser (e.g. [AstroUniBoard](https://github.com/xlazam01/AstroUniBoard)) | only the guide camera | this plugin |

## Features (planned)

- **Guide-camera autofocus**: frames come through PHD2 (PHD2 keeps the guide camera), HFR from
  N.I.N.A. star detection, V-curve fit, backlash handling. Advanced Sequencer instruction
  *Autofocus guide camera* and a button in the plugin panel. Settle time after guiding resumes is configurable.
- **Filter-offset compensation**: with the OAG pick-off in front of the filters, a filter change makes
  N.I.N.A. move the main focuser by the filter offset Δ, which defocuses the guide camera. The plugin
  moves the secondary focuser by −k·Δ (k from a calibration wizard). Temperature and autofocus moves
  of the main focuser are not mirrored: they refocus both cameras.
- Works with any ASCOM focuser as the secondary focuser.

## Status

Planning. Issues and milestones: <https://github.com/xlazam01/SecondaryFocuser-NINA/issues>.
Target: N.I.N.A. 3.x, .NET 8.

## License

GPL-3.0, see [LICENSE](LICENSE).
