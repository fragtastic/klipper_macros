# klipper_macros

Collection of macros for Klipper. Add them to `printer.cfg`.

```cfg
[include mainsail.cfg]

[exclude_object]

[gcode_macro _CLIENT_VARIABLE]
variable_park_at_cancel: True ; allow to move the toolhead to park while execute CANCEL_PRINT [True/False]
gcode:

[include bed_heat_soak.cfg]
[include perform_bed_mesh.cfg]
[include nozzle_prime_line_printer_name.cfg]
[include start_print.cfg]
[include end_print.cfg]

...

```
