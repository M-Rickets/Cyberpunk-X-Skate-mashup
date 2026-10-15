# Night City Shred: setup help (give this file to Claude)

**For the human reading this:** open a chat with Claude (the free version is fine), drag this file
into it and say *"help me set up Night City Shred"*. Claude will walk you through it and can read
anything you paste back (the setup's details, an error, a screenshot). Claude can't click or install
things on your PC from a chat, so you do the clicks and it tells you which ones.

---

## For Claude: what this is and how to help

You're helping a friend of the mod's author install **Night City Shred**, a private, just-for-fun
fan mod that adds skateboarding (built from the game *skate.*) to *Cyberpunk 2077* on PC. It comes
as one program, **NightCityShred-Setup.exe**, with a big **MAKE IT WORK** button. Your job is to
guide them through it step by step, read what they paste and explain what to do next.

How to help well:

- Go one step at a time. Ask what they see on screen before moving on.
- When something fails, ask them to open **details** in the setup window (top right), copy everything
  (click into the text, **Ctrl+A**, **Ctrl+C**) and paste it. Read it before guessing. The messages
  in the troubleshooting table below are the setup's own words.
- If the mod doesn't work in the game, have them close the game and **open the setup again**: it
  checks what loaded the last time the game ran and shows a ✓ or ✗ per piece (see *Checking it
  worked*). Its details say why something didn't load; that's the best thing to have them paste.
- Updates arrive through the same setup program (see *Updates*); there's never a new file to
  download by hand.
- Only use what's in this file and what they paste. If you don't know, say so; don't invent file
  names, settings or buttons.
- Don't suggest downloading modding tools from anywhere except their official GitHub pages (listed
  below), turning antivirus off entirely, or getting *skate.* any way other than its free official
  download. Nothing from *skate.* is included in this mod: the setup reads the player's own copy.
- The player can't break their game with this: **undo everything** puts the game folder back as it
  was (see *Taking it out*).
- On an already modded game, have them click **report** (top of the setup window) **before**
  pressing the big button, and paste or attach the `NightCityShred-report.txt` it saves (see *The mod
  report*). It only reads the game, and it answers most "will this fit?" questions up front.
- On an already modded game, setup leaves the player's own modding tools alone (see *Already
  modded?*). If it flags one as older than tested, don't push them to update it unless the mod
  actually misbehaves: their other mods or an older game version may depend on that version.

---

## What you need

- Windows 10 or 11 (64-bit) and an internet connection.
- **Cyberpunk 2077** (Steam, GOG or Epic) on **patch 2.31**, the newest one. The modding tools only
  work on it: setup reads the game's version first and stops (changing nothing) if it's older.
- **skate.**, free on Steam: <https://store.steampowered.com/app/3354750/>. It has to be fully
  downloaded (Steam says *Play*). It's a big download, so it's worth starting it first. Once setup
  has finished you can uninstall *skate.* again if you need the space (you'd only need it back to
  re-run setup later, for example after a big game update).

## Setting it up

1. **Close Cyberpunk 2077** (and its launcher, if one is open).
2. **Run `NightCityShred-Setup.exe`.**
   - If Windows says *"Windows protected your PC"*, click **More info**, then **Run anyway**. That
     warning appears for any program that isn't signed by a company; this one is a hobby project.
   - If your antivirus removes or blocks it, restore it from the antivirus's quarantine and allow
     that one file. The setup downloads modding tools and writes into the game folder, which some
     antivirus programs treat as suspicious.
3. **Press MAKE IT WORK** (or press Enter). It ticks off five steps:
   1. *Find Cyberpunk 2077*: it looks in Steam, GOG and Epic, and next to itself. If it finds the
      game in more than one place, it lists them and asks which one you play.
   2. *Get the modding tools*: it downloads the newest Cyber Engine Tweaks, RED4ext, redscript,
      ArchiveXL, TweakXL, Codeware and Audioware from their official GitHub pages, and the Microsoft
      Visual C++ runtime if the PC's is older than 14.40.33810, which Cyber Engine Tweaks needs (Windows may ask for permission for that).
      Any of these you already have are left as they are (see *Already modded?*).
   3. *Put in Night City Shred*.
   4. *Build the board from skate.*: it reads your *skate.* install and builds the board, the
      tricks, the animations and the sounds. This takes a minute or two.
   5. *Ready to ride*: before saying so, it checks that every file it put in is still there and
      intact (an antivirus sometimes removes modding files right after they're written), that each
      tool's loader files are there, that the runtime is new enough, and that the board, moves and
      sounds were all built. Then it compiles the game's scripts with the mods, the way the game
      will when it starts. If that fails it fixes what it can by itself (leftover files from an older
      redscript, old copies of the tools' scripts, a game script file an old redscript rewrote; all
      kept for undo) and tries again; if it still fails, it asks Steam to check the game's files.
4. **If it stops at step 4 with an orange "!"** and a **GET SKATE. (FREE)** button, *skate.* isn't
   installed yet (or is still downloading). Click that button (it opens *skate.* in Steam), install
   it, wait until Steam says *Play*, then press **MAKE IT WORK** again. It carries on from there.
5. When the button turns green and says **ALL SET!**, you're done. Close the setup. If the last step
   gets a red ✗ instead, the details list what's missing and what to do; usually pressing the button
   again fixes it.

### Checking it worked

After you've played once, close the game and open the setup again. It reads what the game and the
tools wrote while the game ran and shows a ✓ or ✗ for each piece: *Files in place*, *Visual C++
runtime*, *Cyber Engine Tweaks*, *RED4ext and plugins*, *Night City Shred*. If something has a ✗, the
button says **FIX IT**: press it to put back what's missing and rebuild, and open **details** to see
why it didn't load. If the game hasn't been started since setup, those rows stay grey.

### The mod report (for games with lots of mods)

Click **report** at the top of the setup window. Setup looks through the game and writes
`NightCityShred-report.txt` next to itself, then opens it. **It changes nothing in the game**, so
it's safe to run before installing. When the game already has mods and Night City Shred isn't
installed yet, the status line suggests it. Send that file (it hides the Windows user name).

What it covers:

- **Summary** first. *Fix these first* (`! PROBLEM`) would stop the mod or the game. *Setup takes
  care of these* (`> setup`) happen by themselves when the big button is pressed. *Worth a look*
  (`? check`) are usually fine.
- **Game**: the version, other copies on the PC, free disk space, and mod managers. For **Vortex**,
  how many mods it deployed and which Vortex mod each file came from. For **Mod Organizer 2**, the
  mods enabled in its profile. For **REDmod**, the `mods` folder.
- **PC**: Windows, processor, memory, graphics card and video memory, and the Visual C++ runtime.
- **Frameworks**: each tool's version, the oldest that works on 2.31, the version tested with, and
  whether it came from the player, Vortex, setup or an MO2 mod.
- **RED4ext plugins**: every plugin with its version, and whether it loaded the last time the game
  ran, or stopped the game.
- **Cyber Engine Tweaks mods**: whether CET started last time and which key opens its overlay. It
  also names mods that replace a game function Night City Shred listens to, and mods that move the
  camera too.
- **redscript mods**: who else wraps or replaces the game functions Night City Shred wraps, and the
  last compile's errors. Then a **trial compile**: the game's scripts with every mod there plus
  Night City Shred's, compiled into a scratch file. If that fails, it says whether the clash is
  with Night City Shred or already there without it.
- **Tweaks, archives, sounds**: counts, the biggest archives, and the ArchiveXL and TweakXL logs.
  Night City Shred's archives only add new files, and its tweaks only append to 6 shops and 11 loot
  tables, so these don't clash.
- **Keys**: Night City Shred's keys, and other mods' Cyber Engine Tweaks hotkeys or input files on
  the same keys.
- **Loaders and overlays**: extra DLLs in `bin\x64` (dinput8, dxgi and so on) and ReShade.
- **The game while it runs**: which DLLs the running game loaded. Setup reads this when **report** is
  clicked while the game is running. If setup is just left open during play, it reads it by itself
  after about 40 seconds. This shows whether Cyber Engine Tweaks' `version.dll` or Windows' own one
  got loaded. It also lists outside programs that put code into the game, like overlays and VR
  tools. If Windows' own `version.dll` was loaded, one of those got in first and Cyber Engine
  Tweaks can't start.
- **Cyber Engine Tweaks at the game's start**: Night City Shred has a small RED4ext plugin of its own.
  It checks that Cyber Engine Tweaks is in the game when it starts, and starts it itself if the game
  didn't load CET's `version.dll`. The report says which happened. If Windows refused to load CET
  even then, it gives the reason, such as an antivirus or Smart App Control.
- **Crashes**: the game's crashes in the last two weeks, from Windows' event log and crash dumps,
  with the DLL each one happened in. If that DLL belongs to a mod, the report names the mod.
- **Last log lines**: the end of the RED4ext, Cyber Engine Tweaks, redscript and Night City Shred
  logs.
- **Saves**: how many, their sizes, and the newest one's level, lifepath and game version.

A **red4ext\plugins folder that isn't a RED4ext plugin** is a common cause of a crash before the
first frame. A tool for another game installed there by mistake is a typical example: UE4SS is for
Unreal Engine games. RED4ext loads every DLL in that folder into Cyberpunk, so their code runs even
though RED4ext then rejects them. Setup moves such a folder aside, unless Vortex put it there. In
that case, disable that mod in Vortex and deploy.

When helping from a report, start with the summary. Things under *Setup takes care of these* need
nothing from the player. With Vortex, if setup replaces an old framework, Vortex later notices the
changed file. The player should keep the changed file and update that mod in Vortex. With MO2, a
framework inside an MO2 mod is loaded over the game folder's, so an old one there has to be updated
or disabled in MO2: setup can't change it.

### Already modded?

If the game already has some of those modding tools (from Vortex, Nexus downloads or anything else),
setup **doesn't touch yours**. (Run **report** first: see *The mod report*.) It only adds the tools that are missing, and undo never removes or
changes the ones you had.

Two exceptions, because those copies can't work on the game as it is now: a tool **made for an
older Cyberpunk 2077** than 2.31 (an old Codeware stops the game at start with *"RED4ext.SDK: Failed
to resolve address for hash …"*; an old Cyber Engine Tweaks never starts), and a plugin the game
stopped loading last time. Setup replaces those with current ones and says so in the details; yours
are kept, so **undo everything** puts them back. An old **redscript** that can't compile the scripts
is replaced the same way.

If one of yours is older than the version Night City Shred was tested with, *Get the modding tools*
shows an orange **!** with an **UPDATE … OLD TOOL(S)** button, and the details say which. The mod is
installed anyway, and an older tool often works fine. Only press the button if the mod misbehaves
**and** your game is up to date: the newest tools need the newest game, and your other mods might
need updates too. Your versions are kept, so **undo everything** puts them back.

Setup never writes into a file that's already there: it replaces it with a new one. That matters for
Vortex, which installs mods as links to its own copies; those copies stay exactly as they were.

**Switching Vortex mods off and on:** if the frameworks are switched off in Vortex, Vortex takes their
files out and the mod loses them. Run setup again: it puts in its own copies. If they're switched on
again later, Vortex deploys its copies over setup's. The next time setup runs, it notices and hands
those frameworks back to Vortex ("Vortex manages it now"). Undo then leaves them alone, and setup
takes out any extra files its own copies had. The simplest setup with Vortex is to leave the
frameworks on in Vortex and keep them updated there. (If
you play through Mod Organizer 2 instead, setup can't see the tools MO2 manages, so it adds its own
copies to the game folder; undo removes them.)

## In the game

1. Start Cyberpunk 2077. The first time, **Cyber Engine Tweaks** asks which key should open its
   overlay: press one (**~** is the usual choice). That overlay is where the mod's own window lives.
2. Load a save from **after the opening** (or play through it). Once the opening has played out,
   **Rogue** messages you that she left a board in your stash.
3. Open the **Backpack**, select the skateboard and **Use** it to equip it.
4. Press **B** to get on the board.

Can't find the board? Open the Cyber Engine Tweaks overlay. The **Night City Shred** window shows
whether the mod's game scripts loaded and whether the board is unlocked, and has an **Unlock now and
get the starter board** button.

### Controls (keyboard and mouse)

| Key | What it does |
| --- | --- |
| B | get on / off the board |
| W / S | push / brake |
| A / D | carve; spin in the air |
| Hold right mouse, move the mouse | flick tricks: pull back, then flick (ollie, kickflips and so on) |
| Arrow keys | the same flick tricks without the mouse (Down then Up = ollie; Down then Up+Left = kickflip) |
| Space | quick ollie |
| F (hold) | grind a rail or ledge |
| Q / E | left / right grab |
| R | modifier (dark catches, slides) |
| Left Shift + A / D | powerslide, revert |
| C (hold) | manual (W + C: nose manual) |
| L | trick book |
| O | take / cancel a skate job from a fixer |
| Middle mouse | swing the camera back behind the board |
| F7 | 90s camcorder (VHS) look on / off |

On a controller: double-tap **LB** to get on, **Y** to get off, left stick steers, pushes and
brakes, right stick does the flick tricks, **LT / RT** grab, **RB** is the modifier, **LB** the
powerslide.

## Updates

Keep `NightCityShred-Setup.exe` (anywhere is fine). Lost it? Every version is in the `updates` folder
of <https://github.com/M-Rickets/Cyberpunk-X-Skate-mashup>: download the newest
`NightCityShred-Setup-<version>.exe`. Whenever you open setup, it checks for a newer
Night City Shred and, if there is one, downloads it in the background and says **Update … is
ready**. Nothing changes until you press **INSTALL UPDATE**: then the new setup replaces the old
one, puts the new version in and runs the same checks before saying **ALL SET**. The **details**
show what's new. (The game must be closed, as for setup.) If the update only changed the mod, the
board and moves built from *skate.* are kept, so *skate.* doesn't need to be installed for it.

## Taking it out

Run `NightCityShred-Setup.exe` again and click **undo everything** (top right; it only shows once
setup has installed something). With the game closed, it removes the mod and every modding tool
setup added, puts back any file setup replaced, and removes the folders it made. Modding tools you
had before setup stay as they are. The Microsoft Visual C++ runtime stays, because other games use
it too.

---

## Troubleshooting

The line at the bottom of the setup window (after the `>`) says what happened. **details** shows the
full log.

| The setup says | What to do |
| --- | --- |
| An orange **!** on *Get the modding tools* with **UPDATE … OLD TOOL(S)** | Some tools you already had are older than tested; everything else is installed. See *Already modded?* before pressing it. |
| *This Cyberpunk 2077 is older than 2.31* | The details say which version it is. Update the game (Steam: right-click Cyberpunk 2077, **Properties → Betas**, make sure it says **None**, and let it update), then press the button again. Setup changed nothing. |
| A *"REDScript compilation has failed"* box when the game starts | Close the game and run setup again: its script check finds the cause and fixes it, or asks Steam to check the game's files. |
| *Not everything is in place yet* (red ✗ on *Ready to ride*) | The details list what's missing and what to do. Missing files: press the button again; if they keep vanishing, restore them from the antivirus's quarantine or allow the Cyberpunk 2077 folder. Old Visual C++ runtime: install it from <https://aka.ms/vs/17/release/vc_redist.x64.exe>. |
| *Found Cyberpunk 2077 in … places* | Pick the copy you actually play (Steam: right-click the game, **Manage**, **Browse local files** shows which folder). **folder** at the top changes it later. |
| *Set up. Start the game once…* | Setup is done but the game hasn't run since. Play once, close the game, then open setup again to see the check. |
| *Cyber Engine Tweaks didn't start* | Its overlay never loaded, so there's no hotkey prompt and no mod. The details say why: usually an antivirus blocking `bin\x64\version.dll`, an old Visual C++ runtime, or setup installed into a different copy of the game than the one you play (click **folder** to pick the right one). Press **FIX IT** after sorting that out. |
| *RED4ext or a plugin didn't load* | The details name the plugin and quote its error. If it says the game version isn't supported, update the game in Steam and press **FIX IT**. |
| *Night City Shred didn't load* | The details quote the reason (often a script error from redscript). Press **FIX IT**; if it comes back, paste the details. |
| *Couldn't find Cyberpunk 2077* | Put `NightCityShred-Setup.exe` inside the Cyberpunk 2077 folder (the one that contains the `bin` folder) and run it from there. To find that folder in Steam: right-click Cyberpunk 2077, then **Manage**, then **Browse local files**. |
| *Close Cyberpunk 2077 first* | The game (or a file it uses) is still open. Close it completely, check the taskbar, then press the button again. |
| *Needs permission for the game folder* | The game is in a folder Windows protects. Press the button again and click **Yes** when Windows asks; setup restarts with permission and carries on by itself. |
| *Almost there! Get skate. (free)…* | Install *skate.* (see step 4 above), then press the button again. |
| *skate. is still downloading* | Wait until Steam says *Play* for *skate.*, then press the button again. |
| A tool's *download failed* (in details) | Check the internet connection (a VPN or a strict firewall can block GitHub) and press the button again. It skips what's already done. |
| *Building from skate. failed* | Paste the details. The full log of that step is in `bin\x64\plugins\cyber_engine_tweaks\mods\NightCityShred\generated\skatelink_log.txt` inside the game folder. Often *skate.* was mid-update: let Steam finish, then press the button again. |
| *Something went wrong* | Paste the details. |

Problems in the game:

| What happens | What to do |
| --- | --- |
| The game crashes on start, or shows an error about RED4ext or redscript, right after a game update | The modding tools need versions that match the game. Run setup again (it fetches the newest tools). If the tools haven't caught up with the new game version yet, wait a few days or use **undo everything** in the meantime. |
| A *"redscript compilation failed"* box | Run setup again (see the setup table above). If it comes back, paste the file `r6\logs\redscript_rCURRENT.log` from the game folder. |
| Pressing B does nothing / *"Not yet…"* / *"Equip a board first…"* | Finish the opening, equip the board from the Backpack, or use **Unlock now and get the starter board** in the Night City Shred window of the Cyber Engine Tweaks overlay. |
| The Night City Shred window says *Game scripts: NOT loaded* | Paste `r6\logs\redscript_rCURRENT.log`. |
| It says *skate. catalog: missing* | The build step didn't finish: run setup again with *skate.* installed. |
| No Cyber Engine Tweaks overlay at all | Close the game and open the setup again: its check says what didn't load and why (see *Checking it worked*). |
| No *"press a key"* prompt from Cyber Engine Tweaks, but its row has a ✓ | Its overlay key was already set (by an earlier install of it), so it doesn't ask again. The details say which key: press it in the game. |
| No message from Rogue | The board unlocks once the opening has played out, in free control. The check's details say whether it had unlocked when the game closed. Otherwise use **Unlock now and get the starter board** in the Night City Shred window of the overlay. |
| *"RED4ext.SDK: Failed to resolve address for hash …"* box, then the game closes | A RED4ext plugin made for an older game version. Open setup with the game closed and press the button: it replaces or moves aside the plugin the game stopped on. |

Where the logs are (all inside the Cyberpunk 2077 folder):

- The setup's log: **details** in the setup window.
- Building from *skate.*: `bin\x64\plugins\cyber_engine_tweaks\mods\NightCityShred\generated\skatelink_log.txt`
- Cyber Engine Tweaks: `bin\x64\plugins\cyber_engine_tweaks\cyber_engine_tweaks.log` (and `.log` files in its `mods\NightCityShred` folder)
- RED4ext: the `red4ext\logs` folder
- redscript: `r6\logs\redscript_rCURRENT.log`
- ArchiveXL / TweakXL: `red4ext\plugins\ArchiveXL\ArchiveXL.log`, `red4ext\plugins\TweakXL\TweakXL.log`

---

## Reference

What setup changes in the game folder:

- `bin\x64\plugins\cyber_engine_tweaks\mods\NightCityShred\`: the mod itself (with its setup
  tool in `setup\`)
- `r6\scripts\NightCityShred\`, `r6\tweaks\NightCityShred\`, `r6\audioware\NightCityShred\`
- `archive\pc\mod\NightCityShred_board.archive` and `NightCityShred_anim.archive`
- The modding tools' own files (`bin\x64`, `red4ext\`, `engine\`, `r6\config\` and so on)
- `NightCityShred-undo\`: what **undo everything** needs (the list of what was added, and copies of
  anything replaced). Leave it alone.

It's fine alongside other mods: it leaves modding tools you already have alone, and anything else it
replaces is copied aside first and put back on undo.

The modding tools (official pages, if anything ever needs checking by hand):

- Cyber Engine Tweaks: <https://github.com/maximegmd/CyberEngineTweaks/releases>
- RED4ext: <https://github.com/wopss/RED4ext/releases>
- redscript: <https://github.com/jac3km4/redscript/releases>
- ArchiveXL: <https://github.com/psiberx/cp2077-archive-xl/releases>
- TweakXL: <https://github.com/psiberx/cp2077-tweak-xl/releases>
- Codeware: <https://github.com/psiberx/cp2077-codeware/releases>
- Audioware: <https://github.com/cyb3rpsych0s1s/audioware/releases>

Setup also accepts `--game "<Cyberpunk 2077 folder>"` on its command line, for a game folder it
can't find by itself.
