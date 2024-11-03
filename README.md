# klipper_macros

Collection of macros for Klipper.

## Installation

Clone the repo for update manager to work with.

```sh
cd ~/printer_data/config
git clone https://github.com/fragtastic/klipper_macros.git
```

Add update manager section to `mainsail.cfg`.

```cfg
[update_manager fragtastic_macros]
type: git_repo
primary_branch: main
path: ~/printer_data/config/klipper_macros
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
