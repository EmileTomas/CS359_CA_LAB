# Where need to be modified

To add `iaddl` instruction, we need to add these part in `seq-full.hcl` below:

| Part to add | Reason                                   |
| ----------- | ---------------------------------------- |
| instr_valid | Add `iaddl` to instruction set           |
| need_regids | Obviously, `iaddl` need do something about register( read and write in specific) |
| need_valC   | We need read the constant number added to register |
| srcB        | Declare we need use rB (register) as one input of ALU |
| dstE        | Declare we need use rB (register) as the output of ALU |
| aluA        | Declare the constant number as one input of ALU |
| aluB        | Declare the register as the second input of ALU |
| set_cc      | This is easy to ignore, notice that iaddl is equal to `irmovl` and `addl `. And addl need update condition codes. |



