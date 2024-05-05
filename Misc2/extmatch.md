The WinDbg `.extmatch *` command returns all extension commands from all extensions. Huge part of these is (surprisingly) undocumented, maybe some day I find the right purpose for them. 
If you want to list loaded extensions, use the `.chain` command.

```
!wdfkd.help
!wdfkd.wdfbp
!wdfkd.wdfchildlist
!wdfkd.wdfcollection
!wdfkd.wdfcommonbuffer
!wdfkd.wdfcompanion
!wdfkd.wdfcrashdump
!wdfkd.wdfdevext
!wdfkd.wdfdevice
!wdfkd.wdfdeviceinterrupts
!wdfkd.wdfdevicequeues
!wdfkd.wdfdmaenabler
!wdfkd.wdfdmaenablers
!wdfkd.wdfdmatransaction
!wdfkd.wdfdriverinfo
!wdfkd.wdfextendwatchdog
!wdfkd.wdffindobjects
!wdfkd.wdfforwardprogress
!wdfkd.wdfgetdriver
!wdfkd.wdfhandle
!wdfkd.wdfhelp
!wdfkd.wdfinterrupt
!wdfkd.wdfiotarget
!wdfkd.wdfldr
!wdfkd.wdflogdump
!wdfkd.wdflogsave
!wdfkd.wdfmemory
!wdfkd.wdfobject
!wdfkd.wdfopenhandles
!wdfkd.wdfpoolusage
!wdfkd.wdfqueue
!wdfkd.wdfrequest
!wdfkd.wdfsearchpath
!wdfkd.wdfsetdriver
!wdfkd.wdfsetfxobjectleakthreshold
!wdfkd.wdfsetlogdisplay
!wdfkd.wdfsettraceprefix
!wdfkd.wdfspinlock
!wdfkd.wdfstring
!wdfkd.wdftagtracker
!wdfkd.wdftaskqueue
!wdfkd.wdftmffile
!wdfkd.wdftraceprtdebug
!wdfkd.wdfumdevstack
!wdfkd.wdfumdevstacks
!wdfkd.wdfumdownirp
!wdfkd.wdfumfile
!wdfkd.wdfumirp
!wdfkd.wdfumirps
!wdfkd.wdfumrefhistory
!wdfkd.wdfumtriage
!wdfkd.wdfusbdevice
!wdfkd.wdfusbinterface
!wdfkd.wdfusbpipe
!wdfkd.wdfwmi
!MachOBinComposition.applehelp
!MachOBinComposition.appleunwdecode
!MachOBinComposition.appleunwind
!MachOBinComposition.close
!MachOBinComposition.enablemachodwarfplugin
!MachOBinComposition.lseek
!MachOBinComposition.read
!MachOBinComposition.write
!ELFBinComposition.GetELFImageActivator
!ELFBinComposition.GetKDumpActivator
!ELFBinComposition.OpenCrashDumpFile
!ELFBinComposition.PrepareServicesForHardwareDebugging
!ELFBinComposition.TargetCompositionInitialize
!ELFBinComposition.TargetCompositionUninitialize
!ELFBinComposition.corephdrs
!ELFBinComposition.cppex
!ELFBinComposition.cppfilt
!ELFBinComposition.die
!ELFBinComposition.dieancestry
!ELFBinComposition.dielocal
!ELFBinComposition.diesym
!ELFBinComposition.dietree
!ELFBinComposition.dumpdebug
!ELFBinComposition.dwaranges
!ELFBinComposition.dwhelp
!ELFBinComposition.dwunwind
!ELFBinComposition.hwlinux
!ELFBinComposition.kdumpdescs
!ELFBinComposition.kdumppagerange
!ELFBinComposition.kdumppfn
!ELFBinComposition.ntauxv
!ELFBinComposition.ntfile
!ELFBinComposition.ntprpsinfo
!ELFBinComposition.ntprstatus
!ELFBinComposition.rustdemangle
!ELFBinComposition.vmcoreinfo
!dbghelp.chksym
!dbghelp.dh
!dbghelp.homedir
!dbghelp.lmi
!dbghelp.stackdbg
!dbghelp.sym
!exts.acl
!exts.atom
!exts.avrf
!exts.bievents
!exts.bipackages
!exts.bitcount
!exts.biworkitems
!exts.cs
!exts.decodeptr32
!exts.decodeptr64
!exts.dllcheck
!exts.dlls
!exts.dlltree
!exts.encodeptr32
!exts.encodeptr64
!exts.envvar
!exts.exrlog
!exts.findthis
!exts.gflag
!exts.globaltokenattr
!exts.hashtable
!exts.heap
!exts.help
!exts.hstring
!exts.hstring2
!exts.kuser
!exts.ldrnode
!exts.mui
!exts.peb
!exts.psmapps
!exts.psmclientapps
!exts.psmtestapps
!exts.psmusageapps
!exts.psr
!exts.rebase
!exts.schema
!exts.sd
!exts.services
!exts.shipassert
!exts.sid
!exts.slist
!exts.stltree
!exts.teb
!exts.time
!exts.tls
!exts.token
!exts.tp
!exts.udeadlock
!exts.urcu
!exts.winrterr
!kext.can_write_kdump
!kext.cbreg
!kext.db
!kext.dc
!kext.dcs
!kext.dd
!kext.diskspace
!kext.dp
!kext.dq
!kext.du
!kext.dw
!kext.eb
!kext.ecb
!kext.ecd
!kext.ecs
!kext.ecw
!kext.ed
!kext.exca
!kext.help
!kext.pci
!kdexts.ablock
!kdexts.acpicache
!kdexts.acpiinf
!kdexts.acpiirqarb
!kdexts.acpiresconflict
!kdexts.acpitable
!kdexts.aest
!kdexts.ahcache
!kdexts.alignmentfaults
!kdexts.alpc
!kdexts.amli
!kdexts.apc
!kdexts.apic
!kdexts.apicerr
!kdexts.arbinst
!kdexts.arbiter
!kdexts.arblist
!kdexts.bcb
!kdexts.biosreslist
!kdexts.blockeddrv
!kdexts.bpid
!kdexts.bugcheckrecovery
!kdexts.bugdump
!kdexts.bushnd
!kdexts.ca
!kdexts.callback
!kdexts.calldata
!kdexts.cchelp
!kdexts.chklowmem
!kdexts.cmci
!kdexts.cmreslist
!kdexts.code12
!kdexts.combine
!kdexts.cpuinfo
!kdexts.cpuquota
!kdexts.cshelp
!kdexts.csrt
!kdexts.cstriage
!kdexts.dbgprint
!kdexts.dblink
!kdexts.ddripsaction
!kdexts.ddripstree
!kdexts.deadlock
!kdexts.defwrites
!kdexts.depnode
!kdexts.devext
!kdexts.devhandles
!kdexts.devinst
!kdexts.devnode
!kdexts.devobj
!kdexts.devpowerstate
!kdexts.devstack
!kdexts.dflink
!kdexts.diskrespin
!kdexts.dma
!kdexts.dmaguard
!kdexts.dmar
!kdexts.dmarla
!kdexts.dmarpt
!kdexts.dpa
!kdexts.dpchistory
!kdexts.dpcs
!kdexts.dpcwatchdog
!kdexts.driveinfo
!kdexts.drivers
!kdexts.drvobj
!kdexts.dskheap
!kdexts.e820reslist
!kdexts.errlog
!kdexts.errpkt
!kdexts.errrec
!kdexts.expirations
!kdexts.exqueue
!kdexts.facs
!kdexts.fadt
!kdexts.fan
!kdexts.filecache
!kdexts.filelock
!kdexts.fileobj
!kdexts.filetime
!kdexts.findautochkblockers
!kdexts.finddata
!kdexts.findfilelockowner
!kdexts.findhandle
!kdexts.findthreads
!kdexts.fpbnode
!kdexts.fpbres
!kdexts.fpsearch
!kdexts.frag
!kdexts.frozen
!kdexts.fxdevice
!kdexts.gbl
!kdexts.gentable
!kdexts.gicc
!kdexts.gicd
!kdexts.gicr
!kdexts.gicr_findapending
!kdexts.halext
!kdexts.halpte
!kdexts.handle
!kdexts.help
!kdexts.hidppd
!kdexts.htrace
!kdexts.ib
!kdexts.icpleak
!kdexts.id
!kdexts.idt
!kdexts.intstats
!kdexts.intsteer
!kdexts.ioapic
!kdexts.ioctldecode
!kdexts.ioresdes
!kdexts.ioreslist
!kdexts.iort
!kdexts.iovdrv
!kdexts.iovirp
!kdexts.ipi
!kdexts.ipmi
!kdexts.irp
!kdexts.irpfind
!kdexts.irpzone
!kdexts.irql
!kdexts.irt
!kdexts.isainfo
!kdexts.its
!kdexts.ivrs
!kdexts.iw
!kdexts.job
!kdexts.joblist
!kdexts.jobtree
!kdexts.kb
!kdexts.kv
!kdexts.kwmi
!kdexts.lbt
!kdexts.loadermemorylist
!kdexts.lockedpages
!kdexts.locks
!kdexts.logonsession
!kdexts.lookaside
!kdexts.lpc
!kdexts.lpit
!kdexts.mapic
!kdexts.mca
!kdexts.memlist
!kdexts.memoryblock
!kdexts.memusage
!kdexts.mpam
!kdexts.mps
!kdexts.msct
!kdexts.mtrr
!kdexts.npcb
!kdexts.npx
!kdexts.nsobj
!kdexts.nstree
!kdexts.numa
!kdexts.numa_hal
!kdexts.ob
!kdexts.object
!kdexts.obsdcache
!kdexts.obtrace
!kdexts.obtracedb
!kdexts.od
!kdexts.openmaps
!kdexts.ow
!kdexts.pagefile
!kdexts.partition
!kdexts.pat
!kdexts.pcicfglog
!kdexts.pcitree
!kdexts.pcm
!kdexts.pcmcia
!kdexts.pcr
!kdexts.pdcclient
!kdexts.pdcclients
!kdexts.pdclog
!kdexts.pdctriage
!kdexts.pfn
!kdexts.pfnperf
!kdexts.pic
!kdexts.platformidle
!kdexts.platformidleaccounting
!kdexts.platformidlecontrol
!kdexts.pnpaction
!kdexts.pnpcompletion
!kdexts.pnpevent
!kdexts.pnplocks
!kdexts.pnpthreads
!kdexts.pnptriage
!kdexts.poaction
!kdexts.poagg
!kdexts.poagglogentry
!kdexts.poaggstate
!kdexts.poaggtarget
!kdexts.pobatt
!kdexts.pocaps
!kdexts.podev
!kdexts.poidle
!kdexts.polist
!kdexts.ponode
!kdexts.pool
!kdexts.poolfind
!kdexts.poolused
!kdexts.poolval
!kdexts.poorder
!kdexts.poperf
!kdexts.popoldev
!kdexts.popolicy
!kdexts.poproc
!kdexts.poprocpolicy
!kdexts.porelation
!kdexts.poreqlist
!kdexts.porequests
!kdexts.posetting
!kdexts.posettings
!kdexts.potrigger
!kdexts.powertriage
!kdexts.pplookaside
!kdexts.ppm
!kdexts.ppmcheck
!kdexts.ppmhelp
!kdexts.ppmidle
!kdexts.ppmidleaccounting
!kdexts.ppmidlecontrol
!kdexts.ppmidlepolicy
!kdexts.ppmlatency
!kdexts.ppmlpscenarios
!kdexts.ppmperf
!kdexts.ppmperfpolicy
!kdexts.ppmsettings
!kdexts.ppmstate
!kdexts.pptt
!kdexts.prcb
!kdexts.process
!kdexts.processfields
!kdexts.processirps
!kdexts.providerinfo
!kdexts.psci
!kdexts.pte
!kdexts.pte2va
!kdexts.ptetree
!kdexts.ptex
!kdexts.ptov
!kdexts.qlockperf
!kdexts.qlocks
!kdexts.quota
!kdexts.range
!kdexts.rawrange
!kdexts.rcu
!kdexts.rdmsr
!kdexts.ready
!kdexts.reg
!kdexts.rellist
!kdexts.remlock
!kdexts.rsdt
!kdexts.running
!kdexts.schedgroup
!kdexts.scm
!kdexts.search
!kdexts.searchpte
!kdexts.secidt
!kdexts.sendnmi
!kdexts.session
!kdexts.silo
!kdexts.smt
!kdexts.socket
!kdexts.spmaccounting
!kdexts.spmpolicies
!kdexts.spmscenarios
!kdexts.spoolsum
!kdexts.spoolused
!kdexts.spr
!kdexts.sprocess
!kdexts.srat
!kdexts.srb
!kdexts.srcu
!kdexts.stacks
!kdexts.swd
!kdexts.sysinfo
!kdexts.sysptes
!kdexts.thread
!kdexts.threadfields
!kdexts.ticks
!kdexts.timer
!kdexts.tokenleak
!kdexts.translator
!kdexts.traplog
!kdexts.trueref
!kdexts.tunnel
!kdexts.tz
!kdexts.tzinfo
!kdexts.ubc
!kdexts.ubd
!kdexts.ube
!kdexts.ubl
!kdexts.ubp
!kdexts.vad
!kdexts.vad_reload
!kdexts.validatelist
!kdexts.verifier
!kdexts.verifyavl
!kdexts.version
!kdexts.vhd
!kdexts.vm
!kdexts.vpb
!kdexts.vtop
!kdexts.walklist
!kdexts.watchdoganalyze
!kdexts.whatperftime
!kdexts.whattime
!kdexts.whea
!kdexts.wheapfa
!kdexts.wnf
!kdexts.wpbt
!kdexts.wsle
!kdexts.xpoolmap
!kdexts.xsave
!kdexts.zombies
```