# pylight

*Highlight multiple patterns at once.*

Read from standard input and color patterns on the standard output.

## Usage

Patterns are read from the command line, by increasing priority, and should be in the form `/PATTERN/COLOR`, where:

- `/` is a single character delimiter
- `PATTERN` is a regular expression
- `COLOR` is a from the available ones

## Example

```sh
# list available colors
./pylight -c

# pylight self-pylight-ning
./pylight <pylight                                            \
    '/\b(import|from|as)\b/magenta'                           \
    '/\b(def|in|while|for|if|else|elif)\b/magenta'            \
    '/\b(or|and|not|continue)\b/magenta'                      \
    '/\b(try|except|finally)\b/magenta'                       \
    '/[a-zA-Z_]+\(/green'  '/\(/none'                         \
    '/\b[0-9]*\b/blue'                                        \
    '/"([^"]|\\")*"/yellow' "/'([^']|\\\')*'/yellow"          \
    '/(\\0[0-9]{,2}|\\x[0-9a-f]{,2})/blue'                    \
    '/#.*/black'
```

## To do

- use argparse
- add more colors
- let use custom colors
