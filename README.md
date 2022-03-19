# MSF-screenrecord-on-MacOS
!!! This vulnerability has been simultaneously discovered or taken by Sudhakar Muthumani of Primefort Private Limited, Khiem Tran and listed as CVE-2022-22600. This is despite I already emailing Apple regarding this back in 2021.
## Affected Versions
As a student, I have limited access to devices in which I can test this vulnerability. The versions I have tested so far are `MacOS 12.1`, `MacOS 12.0`, and `MacOS 11.6.1`.

## POC
Files are in the POC directory. Just run `POC.sh` and a screenshot will be produced without TCC prompt.

## So what is the bug?
MacOS stores permissions based on executables. Thus, if the executable cannot be found after the code has already been loaded into memory, no permissions are restricted.
## Patched versions -- According to Apple
The issue was addressed with improved permissions logic. This issue is fixed in tvOS 15.4, iOS 15.4 and iPadOS 15.4, macOS Monterey 12.3, watchOS 8.5. A malicious application may be able to bypass certain Privacy preferences.
