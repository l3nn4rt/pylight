# pylight

*Highlight multiple patterns at once.*

Read from standard input and color patterns on the standard output.

## Usage

Patterns are read from the command line, by increasing priority, and should be in the form `/PATTERN/COLOR`, where:

- `/` is a single character delimiter
- `PATTERN` is a regular expression
- `COLOR` is one of the available colors

## Example

```sh
# list available colors
./pylight -c

# highlight some patterns
./pylight '/\N{black heart suit}/red' '/py\w*/green' '/i/blue' <<< 'I ♥ pylight-ning'
```

## To do

- handle multi-line patterns
- use argparse
- add more colors
- let use custom colors
