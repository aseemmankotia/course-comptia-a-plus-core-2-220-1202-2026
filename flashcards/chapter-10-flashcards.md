## Chapter 10: Backup Strategies, Safety Procedures, and Environmental Controls — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | 3-2-1 backup rule | 3 total copies of data, on 2 different media types, with 1 copy stored offsite. Exam tip: cloud storage in another region satisfies both the 'different media' and 'offsite' requirements. |
| 2 | Full backup — restore time and storage trade-off | Fastest possible restore (only one backup set needed), but uses the most storage and takes the longest to run each time. It's the baseline all incrementals/differentials are built from. |
| 3 | Incremental backup restore process | Restore requires the last full backup PLUS every incremental backup made since, applied in order. Fastest and smallest to create, but slowest/most complex to restore. |
| 4 | Differential backup restore process | Restore requires only the last full backup PLUS the most recent differential. Backup size grows each day until the next full, but restore is simpler and faster than incremental. |
| 5 | ESD wrist strap internal resistor value | Approximately 1 megohm. Lets static safely discharge to ground while protecting the technician from a direct electrical shock path. |
| 6 | Should you wear an ESD strap when servicing a PSU or CRT monitor? | No — never. These components store high-voltage charge in capacitors even when unplugged; an ESD strap provides a path for that current through your body. Discharge capacitors with a proper tool first. |
| 7 | How to self-ground with no ESD strap/mat available | Touch an unpainted metal part of the case chassis before handling components, and repeat periodically. Exam gotcha: unplugging the PC does NOT remove static already on your body. |
| 8 | First step before servicing any internal PC component | Power down completely and unplug from the wall outlet (not just switch off). Some components can retain power even in a soft-off or sleep state. |
| 9 | Ideal server room relative humidity range | Roughly 40-60% RH. Too low increases ESD risk; too high causes condensation and corrosion. Paired with temperature monitoring as a standard environmental control. |
| 10 | Purpose of an SDS (Safety Data Sheet) | Documents hazards, safe handling, and emergency procedures for chemicals/materials such as toner and cleaning solvents. Must be kept accessible on-site; a specific compliance requirement tested on the exam. |
| 11 | Correct disposal method for batteries and toner cartridges | Never dispose of in regular trash — recycle or dispose of per local hazardous-waste regulations. Many manufacturers offer take-back/recycling programs. Environmental compliance is a distinct tested objective. |
| 12 | Correct lifting technique for heavy equipment | Bend at the knees, keep your back straight, and lift with your legs — never bend at the waist. Also keep cables managed and routed to avoid tripping hazards. |
