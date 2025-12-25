## Brief overview
Guidelines specific to working with WireViz YAML files for creating wiring diagrams and electrical schematics, focused on modification workflows and error resolution.

## Communication style
- Respond directly and technically in the user's language (Slovak for this project), avoiding unnecessary conversation.
- Provide clear explanations of changes without verbose introductions.

## Development workflow
- Always create backup copies of original files before making modifications.
- Test changes immediately using the WireViz tool to generate output files (.html, .png, .svg, .tsv) and ensure they process without errors.

## Coding best practices
- Strictly adhere to WireViz syntax documentation for valid YAML structure.
- Maintain existing connectors and cables sections unchanged unless directly required for new connections.
- Use cable definitions for inter-device connections rather than direct links where possible.
- Define all cables used in connections sections to avoid template errors.

## Error handling strategies
- When WireViz fails, first validate YAML structure using safe_load.
- Check for missing template definitions in connectors/cables sections when unknown template errors occur.
- Compare with working files to identify structural differences.

## Project context
- Use WireViz for Molex connector wiring diagrams with 24 AWG shielded cables.
- Implement pin mappings carefully, mapping connector pins to cable wires according to device specifications.

## Syntax reference
- WireViz syntax documentation: https://github.com/wireviz/WireViz/blob/master/docs/syntax.md
