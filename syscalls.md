# Source for the table below: [psdevwiki.com](https://www.psdevwiki.com/ps4/Syscalls)
Changes, rewriting of text, and other forms of improvements will be made for this table. Such as for example: confirmation of whether or not the syscall ID is accurate for higher firmwares such as 6.72, 7.02, 7.55, 9.00, additional notes, etc.

| Syscall ID | PS4 Firmware | Syscall Name | Syscall Usermode prototype | Notes |
| --- | --- | --- | --- | --- |
| 99 |  <=1.01? | sys\_netcontrol | int sys\_netcontrol(int fd, uint op, void \*buf, uint nbuf) | \- |
| 101 | <=1.01? | sys\_netabort | \- | \- |
| 102 | <=1.01? | sys\_netgetsockinfo | \- | \- |
| 113 | <=1.01? | sys\_socketex | int sys\_socketex(const char \*name, int domain, int type, int protocol) | Like existing socket syscall, but with the addition of a name argument. |
| 114 | <=1.01? | sys\_socketclose | \- | \- |
| 125 | <=1.01? | sys\_netgetiflist | \- | \- |
| 141 | <=1.01? | sys\_kqueueex | \- | \- |
| 379 | \>1.01 <=1.76? | sys\_mtypeprotect | \- | \- |
| 532 | <=1.76? | sys\_regmgr\_call | \- | \- |
| 533 | <=1.01? | sys\_jitshm\_create | \- | Only callable from a jit compiler process, else returns EPERM (0x1) |
| 534 | <=1.01? | sys\_jitshm\_alias | \- | Only callable from a jit compiler/application process, else returns EPERM (0x1) |
| 535 | <=1.01? | sys\_dl\_get\_list | \- | Only callable from a debugger, core dump, or syscore process, else returns EPERM (0x1) |
| 536 | <=1.01? | sys\_dl\_get\_info | \- | Only callable from a debugger, core dump, or syscore process, else returns EPERM (0x1) |
| 537 | <=1.01? | sys\_dl\_notify\_event | \- | Always returns ENOSYS (0x4E) (may only be implemented in devkits) |
| 538 | <=1.01? | sys\_evf\_create | int sys\_evf\_create(char\* name, int flag, struct evFlag \*evf) | \- |
| 539 | <=1.01? | sys\_evf\_delete | int sys\_evf\_delete(int id) | \- |
| 540 | <=1.01? | sys\_evf\_open | int sys\_evf\_open(struct evFlag \*evf) | \- |
| 541 | <=1.01? | sys\_evf\_close | int sys\_evf\_close(int id) | \- |
| 542 | <=1.01? | sys\_evf\_wait | \- | \- |
| 543 | <=1.01? | sys\_evf\_trywait | \- | \- |
| 544 | <=1.01? | sys\_evf\_set | int sys\_evf\_set(int id) | \- |
| 545 | <=1.01? | sys\_evf\_clear | int sys\_evf\_clear(int id) | \- |
| 546 | <=1.01? | sys\_evf\_cancel | int sys\_evf\_cancel(int id) | \- |
| 547 | <=1.01? | sys\_query\_memory\_protection | \- | \- |
| 548 | <=1.01? | sys\_batch\_map | \- | \- |
| 549 | <=1.01? | sys\_osem\_create | \- | \- |
| 550 | <=1.01? | sys\_osem\_delete | \- | \- |
| 551 | <=1.01? | sys\_osem\_open | \- | \- |
| 552 | <=1.01? | sys\_osem\_close | \- | \- |
| 553 | <=1.01? | sys\_osem\_wait | \- | \- |
| 554 | <=1.01? | sys\_osem\_trywait | \- | \- |
| 555 | <=1.01? | sys\_osem\_post | \- | \- |
| 556 | <=1.01? | sys\_osem\_cancel | \- | \- |
| 557 | <=1.01? | sys\_namedobj\_create | \- | \- |
| 558 | <=1.01? | sys\_namedobj\_delete | \- | \- |
| 559 | <=1.01? | sys\_set\_vm\_container | \- | Successful call requires privileges (uid0), else returns EPERM (0x1) |
| 560 | <=1.01? | sys\_debug\_init | \- | \- |
| 561 | <=1.01? | sys\_suspend\_process | int sys\_suspend\_process(int pid) | Successful call requires credentials (td->td\_proc->p\_ucred), else returns EPERM (0x1) |
| 562 | <=1.01? | sys\_resume\_process | int sys\_resume\_process(int pid) | Successful call requires credentials (td->td\_proc->p\_ucred), else returns EPERM (0x1) |
| 563 | <=1.01? | sys\_opmc\_enable | \- | \- |
| 564 | <=1.01? | sys\_opmc\_disable | \- | \- |
| 565 | <=1.01? | sys\_opmc\_set\_ctl | \- | \- |
| 566 | <=1.01? | sys\_opmc\_set\_ctr | \- | \- |
| 567 | <=1.01? | sys\_opmc\_get\_ctr | \- | \- |
| 568 | <=1.01? | sys\_budget\_create | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 569 | <=1.01? | sys\_budget\_delete | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 570 | <=1.01? | sys\_budget\_get | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 571 | <=1.01? | sys\_budget\_set | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 572 | <=1.01? | sys\_virtual\_query | int sys\_virtual\_query(uint64\_t addr, uint64\_t unk, void \*info, uint64\_t info\_size) | \- |
| 573 | <=1.01? | sys\_mdbg\_call | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 574 | <=1.01? | sys\_sblock\_create | \- | \- |
| 575 | <=1.01? | sys\_sblock\_delete | \- | \- |
| 576 | <=1.01? | sys\_sblock\_enter | \- | \- |
| 577 | <=1.01? | sys\_sblock\_exit | \- | \- |
| 578 | <=1.01? | sys\_sblock\_xenter | \- | \- |
| 579 | <=1.01? | sys\_sblock\_xexit | \- | \- |
| 580 | <=1.01? | sys\_eport\_create | \- | \- |
| 581 | <=1.01? | sys\_eport\_delete | \- | \- |
| 582 | <=1.01? | sys\_eport\_trigger | \- | \- |
| 583 | <=1.01? | sys\_eport\_open | \- | \- |
| 584 | <=1.01? | sys\_eport\_close | \- | \- |
| 585 | <=1.01? | sys\_is\_in\_sandbox | \- | \- |
| 586 | <=1.01? | sys\_dmem\_container | \- | Successful call requires privileges (uid0), else returns EPERM (0x1) |
| 587 | <=1.01? | sys\_get\_authinfo | \- | Some functionality requires privileges (uid0) |
| 588 | <=1.01? | sys\_mname | \- | \- |
| 589 | <=1.01? | sys\_dynlib\_dlopen | \- | Always returns ENOSYS (0x4E) (may only be implemented in devkits) |
| 590 | <=1.01? | sys\_dynlib\_dlclose | \- | \- |
| 591 | <=1.01? | sys\_dynlib\_dlsym | int sys\_dynlib\_dlsym(SceKernelModule handle, const char \*symbol, void \*\*addrp) | \- |
| 592 | <=1.01? | sys\_dynlib\_get\_list | int sys\_dynlib\_get\_list(SceKernelModule \*pArray, size\_t numArray, size\_t \* pActualNum) | \- |
| 593 | <=1.01? | sys\_dynlib\_get\_info | int sys\_dynlib\_get\_info(SceKernelModule handle, SceDbgModuleInfo \*pInfo) | Sony has stripped module information since 1.76 FW (STO) \* |
| 594 | <=1.01? | sys\_dynlib\_load\_prx | int sys\_dynlib\_load\_prx(const char \*moduleFileName, size\_t args, const void \*argp, uint32\_t flags, const SceKernelLoadModuleOpt \*pOpt, int \*pRes) | \- |
| 595 | <=1.01? | sys\_dynlib\_unload\_prx | int sys\_dynlib\_unload\_prx(SceKernelModule handle, size\_t args, const void \*argp, uint32\_t flags, const SceKernelUnloadModuleOpt \*pOpt, int \*pRes) | \- |
| 596 | <=1.01? | sys\_dynlib\_do\_copy\_relocations | \- | \- |
| 597 | <=1.01? | sys\_dynlib\_prepare\_dlclose | \- | Contains an exploitable integer overflow on FWs <= 1.76 |
| 598 | <=1.01? | sys\_dynlib\_get\_proc\_param | \- | \- |
| 599 | <=1.01? | sys\_dynlib\_process\_needed\_and\_relocate | \- | \- |
| 600 | <=1.01? | sys\_sandbox\_path | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns EPERM (0x1) |
| 601 | <=1.01? | sys\_mdbg\_service | \- | \- |
| 602 | <=1.01? | sys\_randomized\_path | \- | Some functionality requires privileges (uid0) |
| 603 | <=1.01? | sys\_rdup | \- | Successful call requires privileges (uid0), else returns EPERM (0x1) |
| 604 | <=1.01? | sys\_dl\_get\_metadata | \- | Only callable from a debugger, core dump, or syscore process, else returns EPERM (0x1) |
| 605 | <=1.01? | sys\_workaround8849 | \- | \- |
| 606 | <=1.01? | sys\_is\_development\_mode | \- | \- |
| 607 | <=1.01? | sys\_get\_self\_auth\_info | \- | \- |
| 608 | <=1.01? | sys\_dynlib\_get\_info\_ex | int sys\_dynlib\_get\_info\_ex(int moduleHandle, struct Unk \*unk, int \*destModuleInfoEx) | \- |
| 609 | <=1.01? | sys\_budget\_getid | int sys\_budget\_getid(void) | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 610 | <=1.01? | sys\_budget\_get\_ptype | int sys\_budget\_get\_ptype(int budgetID) | \- |
| 611 | <=1.01? | sys\_get\_paging\_stats\_of\_all\_threads | \- | Successful call requires credentials (td->td\_proc->p\_ucred), else returns EPERM (0x1) |
| 612 | <=1.01? | sys\_get\_proc\_type\_info | int sys\_get\_proc\_type\_info(int \*destProcessInfo) | Only callable from certain processes mainly involving media and JiT |
| 613 | \>1.01 <=1.76? | sys\_get\_resident\_count | int sys\_get\_resident\_count(int pid) | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 614 | <=1.76? | sys\_prepare\_to\_suspend\_process | int sys\_prepare\_to\_suspend\_process(int pid) | Successful call requires credentials (td->td\_proc->p\_ucred), else returns ENOSYS (0x4E) |
| 615 | <=1.76? | sys\_get\_resident\_fmem\_count | int sys\_get\_resident\_fmem\_count(int pid) | Some functionality requires privileges (uid0) |
| 616 | <=1.76? | sys\_thr\_get\_name | int sys\_thr\_get\_name(int threadID) | \- |
| 617 | <=1.76? | sys\_set\_gpo | \- | Only callable on development kit (devkit) units |
| 618 | \>1.76? | sys\_get\_paging\_stats\_of\_all\_objects | \- |  |
| 619 | \>1.76? | sys\_test\_debug\_rwmem | \- |  |
| 620 | \>1.76? | sys\_free\_stack | \- |  |
| 621 | \>1.76? | sys\_suspend\_system | \- |  |
| 622 | \>1.76? | sys\_ipmimgr\_call | \- |  |
| 623 | \>1.76? | sys\_get\_gpo | \- |  |
| 624 | \>1.76? | sys\_get\_vm\_map\_timestamp | \- |  |
| 625 | \>1.76? | sys\_opmc\_set\_hw | \- |  |
| 626 | \>1.76? | sys\_opmc\_get\_hw | \- |  |
| 627 | \>1.76? | sys\_get\_cpu\_usage\_all | \- |  |
| 628 | \>1.76? | sys\_mmap\_dmem | \- |  |
| 629 | \>1.76? | sys\_physhm\_open | \- |  |
| 630 | \>1.76? | sys\_physhm\_unlink | \- |  |
| 631 | \>1.76? | sys\_resume\_internal\_hdd | \- |  |
| 632 | \>1.76? | sys\_thr\_suspend\_ucontext | \- |  |
| 633 | \>1.76? | sys\_thr\_resume\_ucontext | \- |  |
| 634 | \>1.76? | sys\_thr\_get\_ucontext | \- |  |
| 635 | \>1.76? | sys\_thr\_set\_ucontext | \- |  |
| 636 | \>1.76? | sys\_set\_timezone\_info | \- |  |
| 637 | \>1.76? | sys\_set\_phys\_fmem\_limit | \- |  |
| 638 | \>1.76? | sys\_utc\_to\_localtime | \- |  |
| 639 | \>1.76? | sys\_localtime\_to\_utc | \- |  |
| 640 | \>1.76? | sys\_set\_uevt | \- |  |
| 641 | \>1.76? | sys\_get\_cpu\_usage\_proc | \- |  |
| 642 | \>1.76? | sys\_get\_map\_statistics | \- |  |
| 643 | \>1.76? | sys\_set\_chicken\_switches | \- |  |
| 644 | ?>4.05>3.55? | sys\_extend\_page\_table\_pool | int sys\_extend\_page\_table\_pool(void) |  |
| 645 | ?>4.05>3.55?? | sys\_extend\_page\_table\_pool2 | int sys\_extend\_page\_table\_pool2(void) | Duplicate of sys\_extend\_page\_table\_pool. |
| 646 | \>1.76? | sys\_get\_kernel\_mem\_statistics | \- |  |
| 647 | \>1.76? | sys\_get\_sdk\_compiled\_version | \- |  |
| 648 | \>1.76? | sys\_app\_state\_change | \- |  |
| 649 | \>1.76? | sys\_dynlib\_get\_obj\_member | \- |  |
| 650 | \>1.76? | sys\_budget\_get\_ptype\_of\_budget | \- |  |
| 651 | \>1.76? | sys\_prepare\_to\_resume\_process | \- |  |
| 652 | \>1.76? | sys\_process\_terminate | \- |  |
| 653 | \>1.76? | sys\_blockpool\_open | \- |  |
| 654 | \>1.76? | sys\_blockpool\_map | \- |  |
| 655 | \>1.76? | sys\_blockpool\_unmap | \- |  |
| 656 | \>1.76? | sys\_dynlib\_get\_info\_for\_libdbg | \- |  |
| 657 | \>1.76? | sys\_blockpool\_batch | \- |  |
| 658 | \>1.76? | sys\_fdatasync | \- |  |
| 659 | \>1.76? | sys\_dynlib\_get\_list2 | \- |  |
| 660 | \>1.76? | sys\_dynlib\_get\_info2 | \- |  |
| 661 | \>1.76? | sys\_aio\_submit | \- |  |
| 662 | \>1.76? | sys\_aio\_multi\_delete | \- |  |
| 663 | \>1.76? | sys\_aio\_multi\_wait | \- |  |
| 664 | \>1.76? | sys\_aio\_multi\_poll | \- |  |
| 665 | \>1.76? | sys\_aio\_get\_data | \- |  |
| 666 | \>1.76? | sys\_aio\_multi\_cancel | \- |  |
| 667 | \>1.76? | sys\_get\_bio\_usage\_all | \- |  |
| 668 | \>1.76? | sys\_aio\_create | \- |  |
| 669 | \>1.76? | sys\_aio\_submit\_cmd | \- |  |
| 670 | \>1.76? | sys\_aio\_init | \- |  |
| 671 | \>1.76? | sys\_get\_page\_table\_stats | \- |  |
| 672 | \>1.76? | sys\_dynlib\_get\_list\_for\_libdbg | \- |  |
| 673 | ?> 5.07? | sys\_blockpool\_move | \- |  |
| 674 | ?> 5.07? | sys\_virtual\_query\_all | \- |  |
| 675 | ?> 5.07? | sys\_reserve\_2mb\_page | \- |  |
| 676 | ?> 5.07? | sys\_cpumode\_yield | \- |  |
| 677 | ?>= 6.50? (not present on 6.20) | sys\_get\_phys\_page\_size | \- | Not present in PS5 PS4EMU on PS5 FW 2.20. |
