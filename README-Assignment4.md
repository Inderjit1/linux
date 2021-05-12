### Question 1.

Inderjit Bassi - 

Eugene Clewlow - 

### Question 2. dmesg output
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
