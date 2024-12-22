Gallium Kanata
================================================================================

Installation
--------------------------------------------------------------------------------

- To get Gallium Kanata, check out this repository
- Launch `kanata.kbd` with Kanata.
  - You can install Kanata by downloading a
  [pre-built executable][Download Kanata] or use `kanata_macos_arm64` from this repo for M1,M2,M3 CPUs
  - Follow the installation details of your operating system.

## Run Kanata 

Quit from `Karabiner-Elements` if you run it!

`sudo ./kanata_macos_arm64 --cfg ~/personal/arsenik/kanata/kanata.kbd --debug`

You should see something like this: 

```
01:21:33.0846 [INFO] kanata v1.8.0-prerelease-1 starting
01:21:33.0867 [INFO] process unmapped keys: true
01:21:33.0868 [INFO] NOTE: kanata was compiled to never allow cmd
01:21:33.0868 [DEBUG] (1) kanata_parser::cfg::alloc: freeing allocations of length 0
01:21:33.0876 [INFO] config file is valid
01:21:33.0876 [DEBUG] (1) kanata_state_machine::kanata::output_logic::zippychord: zchd reset state
01:21:33.0876 [DEBUG] (1) kanata_state_machine::kanata::output_logic::zippychord: zchd soft reset state
01:21:33.0876 [DEBUG] (1) kanata_state_machine::kanata::output_logic::zippychord: zchd clear historical data
01:21:33.0876 [INFO] Sleeping for 2s. Please release all keys and don't press additional ones. Run kanata with --help to see how understand more and how to disable this sleep.
01:21:35.0927 [INFO] entering the processing loop
01:21:35.0929 [INFO] entering the event loop
01:21:35.0930 [INFO] Init: catching only releases and sending immediately
connected
driver_activated 1
driver_connected 0
driver_version_mismatched 0
01:21:35.7268 [INFO] Starting kanata proper
01:21:35.7269 [INFO] You may forcefully exit kanata by pressing lctl+spc+esc at any time. These keys refer to defsrc input, meaning BEFORE kanata remaps keys.
driver_connected 1
```

[Download Kanata]: https://github.com/jtroo/kanata/releases
