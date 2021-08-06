# commands_parser
Made the ability to parse a string of commands easier.
#### Key Features:
* **Easy**: Designed with simplicity in mind. Uses modern design principle making the code DRY and Extensible.
* **Great Developer Experience**: Being fully typed makes it great for editor support. 
* **There is More!!!**:
    * [host_reader](https://github.com/tybruno/hosts_reader): retreive a list of host from a file or string.
    * [commands_reader](https://github.com/tybruno/commands_reader): retreive a list of commands from a file or string.
    * [parser](https://github.com/tybruno/parsers): Generic Parsers and Abstract classes. This project extends parsers.
## Installation
`pip install "git+https://github.com/tybruno/commands_parser.git#egg=commands_parser`
## Usage
### Example 1
```python
from commands_parser import CommandsParser
commands_str = "show cdp nei, show run | inc boot"

parse_commands = CommandsParser()

commands = parse_commands(commands_str)

print(list(commands)) # ['show cdp nei', 'show run | inc boot']
```
### Example 2

```python
from commands_parser import CommandsParser
commands_str = """show cdp nei
show run | inc boot
"""

parse_commands = CommandsParser()

commands = parse_commands(commands_str)

print(tuple(commands)) # ('show cdp nei', 'show run | inc boot')
```
