### Question 1. For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched. (You may skip this question if you are doing the lab by yourself). 

Inderjit Bassi - 

Eugene Clewlow - I wrote the code to print out exit counts for the 0x4FFFFFFE leaf, for both with ept and without ept.

### Question 2. Include a sample of your print of exit count output from dmesg from “with ept” and “without ept”.

```powershell
# with ept
[Thu May  6 19:44:26 2021] CPUID(0x4FFFFFFF), exits= 2734937, cycles spent in exit= 3861539392
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 0, exits= 2671
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 1, exits= 237071
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 2, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 7, exits= 19903
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 8, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 9, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 10, exits= 390
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 12, exits= 96889
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 13, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 14, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 15, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 18, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 19, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 20, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 21, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 22, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 23, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 24, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 25, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 26, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 27, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 28, exits= 160113
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 29, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 30, exits= 290861
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 31, exits= 913705
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 32, exits= 547219
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 36, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 37, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 39, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 40, exits= 88994
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 41, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 43, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 44, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 45, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 46, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 47, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 48, exits= 145177
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 49, exits= 113314
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 50, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 52, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 53, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 54, exits= 5
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 55, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 56, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 57, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 58, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 59, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 60, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 61, exits= 0
[Thu May  6 19:43:39 2021] CPUID(0x4FFFFFFE), exit number= 62, exits= 0
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Thu May  6 19:43:40 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Thu May  6 19:43:40 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Thu May  6 19:43:40 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Thu May  6 19:43:40 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Thu May  6 19:43:40 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
```

```powershell
# without ept
[Tue May 11 17:48:27 2021] CPUID(0x4FFFFFFF), exits= 5105562, cycles spent in exit= 3313182944
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 0, exits= 992002
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 1, exits= 173902
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 2, exits= 0
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 7, exits= 35379
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 8, exits= 0
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 9, exits= 0
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 10, exits= 382
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 12, exits= 97957
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 13, exits= 0
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 14, exits= 595713
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 15, exits= 0
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 18, exits= 0
[Tue May 11 17:48:39 2021] CPUID(0x4FFFFFFE), exit number= 19, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 20, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 21, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 22, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 23, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 24, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 25, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 26, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 27, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 28, exits= 1923280
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 29, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 30, exits= 245112
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 31, exits= 777131
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 32, exits= 273430
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 36, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 37, exits= 0
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 39, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 40, exits= 89112
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 41, exits= 0
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 43, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 44, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 45, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 46, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 47, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 48, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 49, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 50, exits= 0
[Tue May 11 17:48:40 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 52, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 53, exits= 0
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 54, exits= 5
[Tue May 11 17:48:40 2021] CPUID(0x4FFFFFFE), exit number= 55, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 56, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 57, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 58, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 59, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 60, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 61, exits= 0
[Tue May 11 17:48:41 2021] CPUID(0x4FFFFFFE), exit number= 62, exits= 0
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), exit types are not enabled in the KVM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
[Tue May 11 17:48:41 2021] For CPUID(0x4FFFFFFE), ECX exit value does not exist in the SDM
```


### 3. What did you learn from the count of exits? Was the count what you expected? If not, why not?

The numer of exits increased substantially, particularly invalid page and CR access.
This count is as expected because shadow paging requires a lot of exit types to be enabled to work. It is expected that the number of exits increases substantially.

### 4.What changed between the two runs (ept vs no-ept)?

The number of exits nearly doubled.

Substantial exit type count differences (without ept vs with ept)

EXIT_REASON_EXCEPTION_NMI - 992002 vs. 2671

EXIT_REASON_EXTERNAL_INTERRUPT - 173902 vs. 237071

EXIT_REASON_INTERRUPT_WINDOW - 35379 vs. 19903

EXIT_REASON_INVLPG - 595713 vs. 0 (This is invalid page exiting, required for shadow paging)

EXIT_REASON_CR_ACCESS - 1923280 vs. 160113 (also required for shadow paging)

