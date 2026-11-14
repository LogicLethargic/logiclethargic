# sam.m

**Sam** · BTech CSE · Hyderabad

I take things apart to find out why they work, then write down what I found.

Most of what I've built started as *"why does this even do anything?"* — a bus
operator's tracking page that does nothing useful unless you read its
JavaScript; a media receiver burning a full CPU core writing terminal escape
sequences to a `/dev/tty` nobody was watching; a dictation app that sounded
wrong until the pauses stopped being a fixed rate.

**[portfolio](github.com/LogicLethargic/allsamcaresabout)** ← my site

---

### What I work on

**Systems & the Linux desktop**
GNOME on Fedora, GTK4 + libadwaita, Python, shell tooling. I've gone as deep as
initramfs and Plymouth themes, and I'm fond of small tools that do one job.

**Reverse engineering**
Reading other people's JavaScript to find the API underneath — and their
binaries to find the protocol. Syscall tracing, package-layout analysis, symbol
and string recovery, protocol state machines. Then documenting it so the next
person doesn't have to work it out twice.

**Building**
Offline-first tools that solve my own problems. No API keys, no telemetry, no
network where it isn't needed.

### Selected work

| | |
|---|---|
| **[WriteAlong v2](https://github.com/LogicLethargic/writealong)** | Desktop dictation app. Gaps between words are *computed* per word — think latency, letter count against a superlinear length curve, syllable count, articulation cost for digits and caps, punctuation — then clamped and scaled by pace. Offline TTS via Piper. |
| **[Xiaomi PC Manager on Wine](https://github.com/LogicLethargic/xiaomi-pc-manager-on-wine)** | Reverse-engineered a 766 MB vendor installer into its 21 segments to find out whether a Windows-only phone manager can run on Linux. Only 587 MB is the app — the rest is a kernel driver, a Dokan filesystem layer and an OpenVINO AI service. Got it running far enough to isolate the exact blocker, and mapped the undocumented connectivity stack: BT/WiFi discovery (not mDNS), JSON over Boost.ASIO, and session arbitration with client preemption. |
| **[Panasonic Viera Remote](https://github.com/LogicLethargic/Panasonic-web-remote)** | GTK4 + libadwaita remote control for a TV on the local network. Fedora/GNOME, no dependencies beyond PyGObject. |
| **[Bus Tracker API Notes](https://github.com/LogicLethargic/bus-tracker-api-notes)** | Write-up of an undocumented bus-tracking API reverse-engineered from a tracking page's inline JS — endpoint shape, payload, state machine, and the route-progress geometry to turn GPS fixes into "how far along is the bus". |
| **[PlayBridge Headless](https://github.com/LogicLethargic/playbridge-headless)** | A receiver burning ~1 CPU core while idle, traced to a full-screen dashboard looping terminal escape codes. Fixed with a two-change downstream patch exposing an execution path that already existed, rather than hiding it behind `nohup` or a pty. |

### Reach for

`Python` · `Shell` · `GTK4` · `libadwaita` · `JavaScript` · `Fedora` · `strace` ·
`GDB` · `GJS` · `Rust` (small patches) · `HTML/CSS`

### Currently

Building small things for GNOME, writing up what I take apart, and learning more
systems work than I can currently claim.

### Contact

GitHub is the reliable way to reach me — [open an issue][issues], [start a
discussion][discussions], or just follow along. I'm open to internships and
open-source collaboration.

[issues]: https://github.com/LogicLethargic/writealong/issues
[discussions]: https://github.com/LogicLethargic/sam/discussions

---

<sub>This profile is a work in progress and will keep changing as more of the
work lands.</sub>
