# 1. addi sp,sp,-16
Immediate (-16): 1111 1111 0000
rs1 (sp = x2): 00010
funct3: 000
rd (sp = x2): 00010
Opcode: 0010011
|imm (12 bits)       | rs1 (5 bits)	| funct3 (3 bits)	| rd (5 bits)	| Opcode (7 bits) |
|--------------------|--------------|-----------------|-------------|-----------------|
|111111110000        |	00010       |	000	            |00010        |	0010011         |
---

# 2. sd ra,8(sp)
Immediate (112): 8 (split into imm[11:5] = 0000011 and imm[4:0] = 10000)
rs2 (s0 = x8): 01000
rs1 (sp = x2): 00010
funct3: 011
Opcode: 0100011
| imm[11:5] (7 bits) |	rs2 (5 bits) |	rs1 (5 bits)	| funct3 (3 bits)	| imm[4:0] (5 bits)	| Opcode (7 bits) |
|--------------------|---------------|----------------|-----------------|-------------------|-----------------|
| 0000000            | 	01000        | 	00010         |	011             |	01000             |	0100011         |
---

# 3. li a5,100
immediate: 000000011001
rs1: 0000
rd: 01111
funct3: 000
opcode: 0010011
|imm[11:0]    | rs1   | funct3 | rd    | opcode |
|-------------|-------|--------|-------|--------|
|000000011001 | 00000 | 000    | 01111 | 0010011|
---

# 4. addiw a5,a5,-1
immediate: 111111111111
rs1: 01111
rd: 01111
funct3: 000
opcode: 0011011
|imm[11:0]    | rs1   | funct3 | rd    | opcode |
|-------------|-------|--------|-------|--------|
|111111111111 | 01111 | 000    | 01111 | 0010011|
---

# 5. lui a2,0x1
Immediate [31:12]: 00000000000000000001
rd (a5 = x15): 01100
Opcode: 0010011
|imm[31:12]           | rd    | opcode |
|---------------------|-------|--------|
|00000000000000000001 | 01100 | 0010011|
---

# 6. addi a2,a2,954
Immediate (954): 001110111010
rs1 (sp = x2): 01100
funct3: 000
rd (sp = x2): 01100
Opcode: 0010011
|imm (12 bits)|	rs1 (5 bits) |	funct3 (3 bits)	| rd (5 bits)	| Opcode (7 bits) |
|-------------|--------------|------------------|-------------|-----------------|
|001110111010	| 01100	       | 000              |	01100       |	0010011         |
---

# 7. li a1,100
Immediate [31:12]:000000011001
rd (a5 = x15): 01010
Opcode: 0010011
|imm[31:12]           | rd    | opcode |
|---------------------|-------|--------|
|000000011001         | 01010 | 0010011|
---

# 8. lui a0,0x21
Immediate [31:12]:0000000000100001
rd (a5 = x15): 01010	
Opcode: 0110111
|imm[31:12]           | rd    | opcode |
|---------------------|-------|--------|
|0000000000100001     | 01010	| 0110111|
---

# 9. addi a0,a0,400
Immediate (400): 000110010000
rs1 (sp = x2): 01010
funct3: 000
rd (sp = x2): 01010
Opcode: 0010011
|imm (12 bits)|	rs1 (5 bits) |	funct3 (3 bits)	| rd (5 bits)	| Opcode (7 bits) |
|-------------|--------------|------------------|-------------|-----------------|
|000110010000	| 01010        | 000              |	01010       |	0010011         |
---

# 10. jal ra,10418
Immediate (20 bits):	01000110010001000000
rd (ra):	00001
opcode:	1101111
|imm(20bit)          | rd    | opcode |
|--------------------|-------|--------|
|01000110010001000000| 00001 | 1101111|
---
# 11. li a0,0
Immediate [31:12]:000000000000
rd (a5 = x15): 01010
Opcode: 0010011
|imm[31:12]           | rd    | opcode |
|---------------------|-------|--------|
|000000000000         | 01010 | 0010011|
---

# 12. ld ra,8(sp)
Immediate:000000001000
rd: 00001
rs1: 00010
funct3:011 
Opcode(LD): 0000011 
| imm[11:0]      | rs1   | funct3 | rd    | opcode  |
|----------------|-------|--------|-------|---------|
| 000000001000   | 00010 | 011    | 00001 | 0000011 |
---

# 13. addi sp,sp,16
Immediate (16): 000000010000
rs1 (sp = x2): 00010
funct3: 000
rd (sp = x2): 00010
Opcode: 0010011
|imm (12 bits)       | rs1 (5 bits)	| funct3 (3 bits)	| rd (5 bits)	| Opcode (7 bits) |
|--------------------|--------------|-----------------|-------------|-----------------|
|000000010000        |	00010       |	000	            |00010        |	0010011         |
---

# 14. ret 
Immediate: 0 = 0000000001000 (split into imm[11:5] and imm[4:0] )
rs1: 00001 
rd: 00001
ra: 00001
funct3: 000 
Opcode: 1100111
| imm[11:0]  | rs1   | funct3 | rd    | opcode  |
|------------|-------|--------|-------|---------|
|  00000000  | 00001 | 000    | 00001 | 1100111 |
---

# 15. addiw a5,a5,-1
Immediate (16): 111111111111
rs1 (sp = x2): 01111
funct3: 000
rd (sp = x2): 01111
Opcode: 0011011
|imm (12 bits)       | rs1 (5 bits)	| funct3 (3 bits)	| rd (5 bits)	| Opcode (7 bits) |
|--------------------|--------------|-----------------|-------------|-----------------|
|111111111111        |	01111       |	000	            |  01111      |	0011011         |
---
