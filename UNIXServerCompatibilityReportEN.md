# radare2 bugs and test vault for UNIX servers

Radare2 bugfix issies and build log on UNIX servers and Embedded Linux machines, it is not testing on workstation environment. previous repository: `github.com/unixfreaxjp/radare2test`

## about:

[bugfix issuer](https://github.com/radareorg/radare2/issues?q=is%3Aissue+author%3Aunixfreaxjp+)/tester: @unixfreaxjp
OS: Linux, FreeBSD, OpenBSD, cpu: arm, armel, mips, mipsel, mips64, mips64el, arm64, ppc, sparc, sh4, m68k, x86_64 and x86.
extra: Solaris (sparc)

---

# radare2 for UNIX/Linux servers support in 2020 (attention: r2jp community)

Translation of the [r2jp/doc in here](https://github.com/radareorg/r2jp/blob/master/UNIXServerCompatibilityReportJP.md)

## Background

I would like to conclude radare2 compatibility test results so far and summarize the for UNIX server versions that are not supported. The range for tests is from version 3.9.0 to the 4.4.0 and now in progress testing for [radare2 version 4.5.0](https://github.com/radareorg/radare2/releases/tag/continuous).

The background is, we had a serious meeting with pancake on December 2019 (@SECCON 2019) in Tokyo and discussed we should be clear on which server systems that can be committed to be supported for test and bugdix and which are not for this year (2020).

The conclusion is as follows. The contents was initially written for R2JP/r2 Japanese comunity as standard deployment guide for NIX servers and native embedded Linux devices, but now is shared publicly as reference.

---

## Support information

Conclusion of versions that are currently supported and those that are not:

*) unsupported = Has not been supported since 2020, supported = will be supported until firther notice, core= r2 package/without plug-in

```
FreeBSD 9 :  unsupported, see: https://twitter.com/malwaremustd1e/status/1211930394628509697
FreeBSD 10 : unsupported, see: https://twitter.com/malwaremustd1e/status/1211930394628509697
FreeBSD 11 : supported, core : OK , r2ghidra: NG, r2dec NG 
FreeBSD 12 : supported, core : OK , r2ghidra: NG, r2dec NG 
Debian Wheezy: unsupported, see: https://twitter.com/malwaremustd1e/status/1215954152137740288
Debian Jessie: supported, core : OK , r2ghidra: NG, r2dec OK 
Debian Stretch: supported, core : OK , r2ghidra: NG, r2dec OK 
Debian Buster: supported, core: OK, r2ghidra: PENDING, r2dec PENDING 
Tsurugi Linux SECCON edition (ISO): supported, core : OK , r2ghidra: OK, r2dec OK
Tsurugi Linux 2020 March release (ISO, OVA): (TBA、/ in test)
NetBSD and OpenBSD (TBA、/ in test)
```
---

## Details of issues from tests in NIX servers OS↓(v4.3.0 to v4.4.0 base / core) so far:

Listed problems  in evaluation:
- All supported versions for the above tests are for x64 bit CPUs,  x32bit CPU servers are currently uncommitted for testing and bugfix issue escalation, r2jp users is advised to use the `radare2 4.0.0-git` version for x86_32. The 32bits for non Intel native buiild will be supported in an OS version as long as that version is on supported period in their distribution (`LTSE` for Debian, `LTS' for CentOS, `Production Releases` for FreeBSD, etc).
- r2ghidra fails to compile in Debians before Buster, and I get `isnan` `isinf` errors w/ "ambiguous" flag, it's a CPP compatibility issue on GCC lib-error on coding layer, currently r2ghidra has no solution for this.
- r2ghidra plugins failed completely on CPP library compatible in BSD platforms. Due the BSD platforms is currently out of support context by radare plugin developers.
- Throughout the BSD test scheme, r2dec is having issues of building "duktape", under same development status as previous point.
- FreeBSD x32 is currently not supported, but the latest result is as below ↓

      FreeBSD 9.x-12.x on x86,: core = OK ,: r2ghidra = NG, r2dec = NG.
- The Debian Stretch x32 test is no longer committed, but the latest result is as are below ↓

      Debian Stretch x86,: core = OK ,: r2ghidra = NG, r2dec = OK.
- OpenBSD is still on evaluation. I will report the information again.
- We will inform you about the latest version of NetBSD later, 

---

## Information about the latest stable version (for Linux / BSD servers)

(1) After the below shown versions, x64 bit is architecture that is supported.
```
~/radare2-STABLE]$ r2 -v
radare2 4.2.0-git 23842 @ freebsd-x86-64 git.4.1.1-128-g3c788a496
commit: 3c788a49674d2e1c0e8ddbe6cce52ab4a9bcf818 build: 2020-01-16__14:06:39
```
*) Of the above versions pdc, r2decthe r2ghidra plug-in status is as per contents on "Details of issues".

[The package is here](https://github.com/radareorg/radare2/releases/tag/4.2.0).

(2) For x32Bits of FreeBSD / OpenBSD / Legacy systems for Intel or AMD, and embedded architecture.

Please use the following version, the r2 core program is proven working on the systems:
```
radare2 4.0.0-git 23215 @ linux-x86-32 git.3.9.0-20-gd112883
commit: d112883c5ad7309ca577373639281bb8e57d9988 build: 2019-09-20__21:47:04

radare2 4.0.0-git 23226 @ freebsd-x86-32 git.3.9.0-20-gd112883
commit: d112883c5ad7309ca577373639281bb8e57d9988 build: 2019-09-20__21:55:04

radare2 4.0.0-git 23449 @ linux-x86-64 git.3.9.0-20-gd112883
commit: d112883c5ad7309ca577373639281bb8e57d9988 build: 2019-09-20__21:38:58

radare2 4.0.0-git 22926 @ freebsd-x86-64 git.3.9.0-20-gd112883c5
commit: d112883c5ad7309ca577373639281bb8e57d9988 build: 2019-09-20__12:53:49
```
↑ The decompilers plug-ins of the above versions is pdc (all OS and arch) and r2dec (Linux only).

[The package is here](https://github.com/radareorg/radare2/releases/tag/4.0.0).

---

## Stable OS integration information.

Tsurugi [SECCON 2019 Special Edition](https://blog.0day.jp/p/20191218.html) is the first stable Linux distribution with r2, pdc, r2ghidra and r2dec integration.

```
radare2 4.1.0-git 24455 @ linux-x86-64 git.4.0.0-235-g982be50
commit: 982be504999364c966d339c4c29f20da80128e14 build: 2019-12-17__10:29:05
```

- (core: OK ,: r2ghidra = OK, r2dec = OK)
- VM can be installed with ISO, so you can also install the VM on the x32 server.
- We will add information as soon as we confirm the test results for other Tsurugi Linux versions.
- Currently the retdec decompiler integration is under test and development.

---

## About past radare2test / bug fix / exam status

Below is the current test we have:

- On testing now ⇒ [radare2_4.5.0-git](https://github.com/radareorg/radare2/releases/tag/continuous)
- 4.4.0 (Slow performance (heavy) with minor build "warnings", bug fix in 4.5.0 release)
- 4.3.0 (There are slight build bugs and seems it is fixed in the 4.5.0 release)

*) List of [r2 release information for reference](https://github.com/radareorg/radare2/releases)

---

## EOL information of supported OS distribution

In 2020 a plan for UNIX support was created by referring to the following information from various OS distributions support information:
- [FreeBSD supported versons (Production RELEASE)](https://www.freebsd.org/security/security.html#sup)
- [Linux Debian supported versions (LTSE)](https://wiki.debian.org/LTS/Extended)
- [OpenBSD supported versions](https://marc.info/?l=openbsd-announce) | [or Web site](https://www.openbsd.org/plus.html)
- [NetBSD supported versions](https://www.netbsd.org/releases/release-map.html#release)
- [Tsurugi Linux check versions (CHANGELOG)](https://tsurugi-linux.org/documentation_tsurugi_linux_changelog.php#)

---
*) The above contents are updated regularly, they may change.

unixfreaxjp@tsurugiseccon:~$ date Sat May 30 19:29:59 JST 2020
