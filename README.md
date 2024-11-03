# klipper_macros

Collection of macros for Klipper.

## Installation

Add update manager section to `mainsail.cfg`.

```cfg
# Custom macros update_manager entry
[update_manager CustomMacros]
type: git_repo
primary_branch: main
path: ~/printer_data/config/MACROS
origin: https://github.com/fragtastic/klipper_macros.git
is_system_service: False
```

## Usage

Add them to `printer.cfg`.

```cfg
[include mainsail.cfg]

[exclude_object]

[gcode_macro _CLIENT_VARIABLE]
variable_park_at_cancel: True ; allow to move the toolhead to park while execute CANCEL_PRINT [True/False]
gcode:

[include klipper_macros/bed_heat_soak.cfg]
[include klipper_macros/perform_bed_mesh.cfg]
[include klipper_macros/nozzle_prime_line_printer_name.cfg]
[include klipper_macros/start_print.cfg]
[include klipper_macros/end_print.cfg]
...

```
