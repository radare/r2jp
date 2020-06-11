# r2jp とは？

---

## r2jp = Japanese Community of radare2　

repo/ホームページURL
```
https://github.com/radareorg/r2jp
```

ロゴ

[![](http://bit.ly/2zfKbzD)](http://bit.ly/2zfKbzD)


r2jpは日本国内のradare2ソフトが大好きなユーザを集めたコミュニティであり、ここでradare2に対しての日本国内ユーザのサポート、

イベントと技術交換などのやり取りを行っております。

r2jpのミッションの目的は下記の内容を対応が出来るように日々努力しています。
```
- 質問/Q&Aの対応 （日本語）、
- 開発（プラグイン、追加機能、アイデア）、
- 日本語のドキュメンテーション、
- ワークショップ、トレーニング、プレゼンテーション、など。
```

現在対応方法について、具体的に
```
内容によって、radare2のベテラン・ユーザーが入門と便利な使い方をデモさせます、
イベントでのQ/Aの形で質問を回答致します、そして時間が出来たらhowto手順を作成します。
なお、一年間1回のミーティングも行いますので、その時にもコミュニティが集まって、面白い新しい使い方のプレセンテーションを行います。
```

---
**現在radare2でアセンブリ/ディスアセンブリが可能なアーキテクチャの対応一覧**
```
$ rasm2 -L
_dAe  8 16       6502        LGPL3   6502/NES/C64/Tamagotchi/T-1000 CPU
__A_  8 32       6502.cs     BSD     Capstone mos65xx CPU disassembler (not supported)
adAe  8          8051        PD      8051 Intel CPU
_dA_  32         amd29k      LGPL3   AMD 29k RISC CPU (by deroad)
_dA_  16 32      arc         GPL3    Argonaut RISC Core
a___  16 32 64   arm.as      LGPL3   as ARM Assembler (use ARM_AS environment) (by pancake)
adAe  16 32 64   arm         BSD     Capstone ARM disassembler
_dA_  16 32 64   arm.gnu     GPL3    Acorn RISC Machine CPU
_d__  16 32      arm.winedbg LGPL2   WineDBG's ARM disassembler
adAe  8 16       avr         GPL     AVR Atmel
adAe  16 32 64   bf          LGPL3   Brainfuck (by pancake, nibble) v4.0.0
_dA_  32         chip8       LGPL3   Chip8 disassembler
_dA_  16         cr16        LGPL3   cr16 disassembly plugin
_dA_  32         cris        GPL3    Axis Communications 32-bit embedded processor (by pancake)
adA_  32 64      dalvik      LGPL3   AndroidVM Dalvik
ad__  16         dcpu16      PD      Mojang's DCPU-16
_dA_  32 64      ebc         LGPL3   EFI Bytecode (by Fedor Sakharov)
adAe  16         gb          LGPL3   GameBoy(TM) (z80-like) (by condret)
_dAe  16         h8300       LGPL3   H8/300 disassembly plugin
_dAe  32         hexagon     LGPL3   Qualcomm Hexagon (QDSP6) V6 (by xvilka)
_d__  32         hppa        GPL3    HP PA-RISC
_dAe             i4004       LGPL3   Intel 4004 microprocessor
_dA_  8          i8080       BSD     Intel 8080 CPU
adA_  32         java        Apache  Java bytecode
_d__  32         lanai       GPL3    LANAI
_d__  8          lh5801      LGPL3   SHARP LH5801 disassembler
_d__  32         lm32        BSD     disassembly plugin for Lattice Micro 32 ISA (by Felix Held)
_dA_  8 32       m680x       BSD     Capstone M680X Disassembler
_dA_  32         m68k        BSD     Capstone M68K disassembler
_dA_  32         malbolge    LGPL3   Malbolge Ternary VM (by condret)
_dA_  32         mcore       LGPL3   Motorola MCORE disassembler
_d__  16         mcs96       LGPL3   condrets car
adAe  16 32 64   mips        BSD     Capstone MIPS disassembler
adAe  32 64      mips.gnu    GPL3    MIPS CPU
_dA_  16         msp430      LGPL3   msp430 disassembly plugin
_dA_  32         nios2       GPL3    NIOS II Embedded Processor
adA_  16 32 64   null        MIT     no disassemble (by pancake) v1.0.0
_dA_  32         or1k        LGPL3   OpenRISC 1000
_dAe  8          pic         LGPL3   PIC disassembler
_dAe  32 64      ppc         BSD     Capstone PowerPC disassembler (by pancake)
_dA_  32 64      ppc.gnu     GPL3    PowerPC
_d__  32         propeller   LGPL3   propeller disassembly plugin
_dA_  8 16       pyc         LGPL3   PYC disassemble plugin
_dA_  32 64      riscv       GPL     RISC-V
_dAe  32         rsp         LGPL3   Reality Signal Processor
_dAe  32         sh          GPL3    SuperH-4 CPU
_dA_  8 16       snes        LGPL3   SuperNES CPU
_dAe  32 64      sparc       BSD     Capstone SPARC disassembler
_dA_  32 64      sparc.gnu   GPL3    Scalable Processor Architecture
_d__  16         spc700      LGPL3   spc700, snes' sound-chip
_dA_  32         sysz        BSD     SystemZ CPU disassembler
_dA_  32         tms320      LGPLv3  TMS320 DSP family (c54x,c55x,c55x+,c64x)
_dA_  32         tricore     GPL3    Siemens TriCore CPU
_dAe  32         v810        LGPL3   v810 disassembly plugin (by pancake)
_dAe  32         v850        LGPL3   v850 disassembly plugin
_dAe  8 32       vax         GPL     VAX
adAe  32         wasm        MIT     WebAssembly (by cgvwzq) v0.1.0
_dA_  32         ws          LGPL3   Whitespace esotheric VM
a___  16 32 64   x86.as      LGPL3   Intel X86 GNU Assembler
_dAe  16 32 64   x86         BSD     Capstone X86 disassembler
a___  16 32 64   x86.nasm    LGPL3   X86 nasm assembler
a___  16 32 64   x86.nz      LGPL3   x86 handmade assembler
_dA_  16         xap         PD      XAP4 RISC (CSR)
_dA_  32         xcore       BSD     Capstone XCore disassembler (by pancake)
_dAe  32         xtensa      GPL3    XTensa CPU
adA_  8          z80         GPL     Zilog Z80 (by condret)
$ r2 -v
radare2 4.5.0-git 24737 @ freebsd-x86-64 git.4.4.0-253-gae883f0cd
commit: ae883f0cd3b12da0272f1471cab82c2e75cd1575 build: 2020-06-10__19:54:43
```

---
**radare2プロジェクトの全般リンク（サイト、資料、ダウンロード、使う方、など）**

- site [https://www.radare.org/](https://www.radare.org/) or [http://rada.re/](http://rada.re/)
- releases [https://github.com/radare/radare2/releases](https://github.com/radare/radare2/releases)
- dev/source: [https://github.com/radare/radare2](https://github.com/radare/radare2)
- doc [http://rada.re/vdoc/](http://rada.re/vdoc/)
- book [https://radare.gitbooks.io/radare2book/content/](https://radare.gitbooks.io/radare2book/content/)
- wiki [https://r2wiki.readthedocs.io/en/latest/](https://r2wiki.readthedocs.io/en/latest/)
- etc documentaton [http://radare.today/posts/radare2-is-documented/](http://radare.today/posts/radare2-is-documented/)
- blog [http://radare.today](http://radare.today)
- installers [http://radare.mikelloc.com/list](http://radare.mikelloc.com/list)
- r2con conference [https://rada.re/con/](https://rada.re/con/) or [https://github.com/radareorg/r2con](https://github.com/radareorg/r2con)
- web demo [http://cloud.rada.re](http://cloud.rada.re) (今メインテナンス中)
- ctf tips [http://radare.today/posts/using-radare2/](http://radare.today/posts/using-radare2/)
- devcode CLang checks (Jenkins) [http://ci.radare.org/job/radare2-scan-build/](http://ci.radare.org/job/radare2-scan-build/)
- twitter @radareorg [https://twitter.com/radareorg](https://twitter.com/radareorg)
- [!!NEW!! radare2 UNIX servers compatibility info, ～April 2020](https://github.com/radareorg/r2jp/blob/master/UNIXServerCompatibilityReportJP.md)
---
 
r2jp のイベント情報
```
1. 2017年11月02日「radare2」ワークショップ AVTokyo 2017 (by pancake)
2. 2018年08月31日 radare2JP/[r2jpのOB会イベント]⇒obkai20180831.md
3. 2018年09月07日 r2jpチームからR2CON 2018コンファレンスでのプレゼンテーション (unixfreaxjp/Unpacking the Non-Unpackable)
4. 2018年12月23日 SECCON 2018 CTF YOROZUワークショップでr2con 2018のレポートとv3.1.2でソフトウエア解析入門
5. 2019年12月21日 SECCON 2019のワークショップでradare2のデコンパイラーの報告とデモを行い、r2ghidra-dec、r2decとpdcの紹介とデモ
6. 2019年12月21日 radare2JP/[r2jpのOB会イベント(SECCON 2019後)]⇒obkai20191221.md
```
 
サイトのメインテナー
```
@trufae @tessy_jp @unixfreaxjp @luffykuroneko (r2jp)
```

オブザーバー
```
@sonodam (r2jp)
```
---


