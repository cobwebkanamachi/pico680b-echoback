# pico680b-echoback
This is an echoback test asm routine intended for test picobug.
picobug is this.
https://github.com/simple-circuit/picobug

usage:
<PRE>
1. Save asm file with copy and paste from this repo's pdf.
2. If you saved as A.ASM, assemble it with assembler.
   I used a68 (git clone is suitable, but should avoid zip download..)
3. > a68 A.ASM -l A.lst -s A.s19
4. Check A.s19 is not empty or a68 noticed no error.
5. Attach picobug to usb.
6. open teraterm of SimpleCRT.exe or favarite.
7. put L and send A.s19 with teraterm or your term.
8. J 0100
9. You could do echoback test.
</PRE>

code documentation:
These are all.<BR>
1.Please read: https://www.xenesis.jp/2022/05/altair-680-basic/ esp. POLCAT, INCH.<BR>
2.Please read: https://github.com/simple-circuit/picobug/blob/main/sim680b_rev1.ino <BR>
<PRE>
// UART Status 0xF000 Read Only, Bit-1 Transmit Ready, Bit-0 Receive Ready
//      Use: LDAA $F000 or LDAB $F000
// UART Write Data 0xF001
//      Use: STAA $F001 or STAB $F001
// UART Read Data 0xF003
//      Use: LDAA $F003, LDAB $F003, or ANDB $F003
</PRE>
essence: Mnemonic and aciacs, aciada, straps are tightly binded.:)

Enjoy!!

