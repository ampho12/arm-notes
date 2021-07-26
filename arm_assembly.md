
# Syntax

```
{symbol} {instruction | directive | pseudo-instruction} {; comment}
```

All three are optional
- `symbol` is usually a label for an address (example label for a function or to create if else statements)
- `directive`
- `pseudo-instructions` for the assembler


## Flexible Second Operand (Operand2)
The second operand in arm instructions is usually 'flexible'. It spans 12 bits. It can be:
- **constant**: This can be any value that can be produced by right-rotating an 8-bit value by an any even number within a 32-bit word. The decimal value of remaining 4 bits is doubled to determine number of bits to rotate right by.

- **Register with optional shift** 


### Constant
The 12 bits are split as 8 bits for the value and 4 for the right rotation. Since we are rotating right by an even amount, we can rotate 0, 2, 4, ..., 28, 30 bits only(rotating 32 bits is equivalent to rotating 0 bits). Thus with 4 bits, we have the valus 0 through F, which are multiplied by 2 and then used as the number of bits to roate right.

### Syntax
A `\#` is used followed by the constant value (eg `#93`, `#0xFF`) 


### Register with shift 

