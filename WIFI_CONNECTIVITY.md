Landroid S — WiFi Connectivity & Pairing

This document describes the complete, working network and pairing setup for the Worx Landroid S, including the Ziggo modem/router, TP-Link Deco mesh network, dedicated 2.4 GHz WiFi network, garden coverage, charging station, and the Landroid app pairing procedure.

The most important discovery is that the Landroid does not simply pair as soon as it can see the WiFi network. The mower must first be placed into the correct pairing state by holding the OK button until the red/blue exclamation indicator becomes steady.

⸻

1. System Overview

The working setup consists of:

                         INTERNET
                            │
                            │
                     ┌──────┴──────┐
                     │ Ziggo modem │
                     │ / router    │
                     └──────┬──────┘
                            │
                       Ethernet
                            │
                 ┌──────────┴──────────┐
                 │ TP-Link Deco        │
                 │ Metering cabinet    │
                 │                     │
                 │ WiFi:               │
                 │ Ziggo-...-extension │
                 │ 2.4 GHz             │
                 └──────────┬──────────┘
                            │
                       Deco mesh
                       / WiFi backhaul
                            │
                 ┌──────────┴──────────┐
                 │ TP-Link Deco        │
                 │ Garden              │
                 │                     │
                 │ Ziggo-...-extension │
                 │ 2.4 GHz             │
                 └──────────┬──────────┘
                            │
                         WiFi
                            │
                  ┌─────────┴─────────┐
                  │   Landroid S      │
                  │                   │
                  │   Charging        │
                  │   station         │
                  └───────────────────┘

The purpose of the two Deco units is to provide reliable WiFi coverage from the house/metering cabinet into the garden.

The Landroid connects to the 2.4 GHz WiFi network, rather than the 5 GHz network.

⸻

2. Network Infrastructure

2.1 Ziggo modem/router

The Ziggo modem/router provides the primary Internet connection.

The TP-Link Deco system is connected to the Ziggo network.

The exact Ziggo SSID/password should not be documented in this repository. The SSID used for the Landroid setup can be referred to generically as:

Ziggo-<network>-extension

Do not commit the actual WiFi password to GitHub.

⸻

3. TP-Link Deco — Metering Cabinet

The first TP-Link Deco unit is located in the metering cabinet.

It is connected to the Ziggo modem/router using an Ethernet cable.

Conceptually:

Ziggo modem/router
       │
       │ Ethernet
       ▼
TP-Link Deco #1
(metering cabinet)

This Deco acts as the connection between the Ziggo network and the Deco mesh.

Its WiFi network is the dedicated network used for the garden connection:

Ziggo-<network>-extension

The Deco system is configured so that the Landroid can use the 2.4 GHz portion of this network.

⸻

4. TP-Link Deco — Garden

A second TP-Link Deco unit is positioned in the garden, within reliable wireless range of the first Deco.

Conceptually:

                    House
                     │
             ┌───────┴────────┐
             │ TP-Link Deco #1│
             │ Metering cabinet
             └───────┬────────┘
                     │
                Deco WiFi
                 backhaul
                     │
             ┌───────┴────────┐
             │ TP-Link Deco #2│
             │ Garden         │
             └───────┬────────┘
                     │
                  2.4 GHz
                     │
                Landroid S

The second Deco provides WiFi coverage close to the Landroid’s charging station.

The objective is not merely to have WiFi somewhere inside the house, but to ensure that the Landroid has a sufficiently strong and stable WiFi connection at its charging station in the garden.

⸻

5. Dedicated 2.4 GHz WiFi Network

The Landroid setup uses a dedicated Ziggo/Deco SSID:

Ziggo-<network>-extension

The important characteristic is that the network used during pairing must provide 2.4 GHz WiFi.

During troubleshooting, 5 GHz was disabled on the TP-Link Deco network so that the Landroid would not encounter a 5 GHz-only configuration.

The recommended configuration for troubleshooting/pairing is therefore:

WiFi
├── 2.4 GHz: ENABLED
└── 5 GHz: DISABLED during initial pairing

Once the Landroid has successfully joined the network, the network can potentially be reconfigured depending on the capabilities of the particular Landroid and Deco configuration. However, keeping the network explicitly 2.4 GHz during setup removes an important source of ambiguity.

Why 2.4 GHz?

The Landroid’s WiFi hardware is designed around 2.4 GHz WiFi rather than modern 5 GHz-only configurations.

2.4 GHz also has substantially better propagation through walls and across garden distances than 5 GHz, making it appropriate for a mower operating outside the house.

⸻

6. Position of the Landroid During Pairing

The Landroid should be placed inside its charging station during the pairing procedure.

The mower should not merely be somewhere in the garden.

The required physical state is:

              Charging station
          ┌──────────────────────┐
          │                      │
          │     Landroid S       │
          │       ──────         │
          │      contacts        │
          └──────────┬───────────┘
                     │
                charging contacts

The Landroid is wheeled into the charging station so that the mower’s charging contacts connect with the contacts on the station.

The charging station should show its normal green status light.

⸻

7. Powering On the Landroid

Once the mower is physically in the charging station:

1. Ensure the charging contacts are connected.
2. Switch the Landroid ON.
3. Confirm that the mower is powered up.
4. Confirm that the battery/status indication appears normal.
5. There should not necessarily be an immediate pairing indication.

At this point, the crucial step is to put the mower into pairing mode.

⸻

8. Entering Pairing Mode

The Critical Step

Press and hold the OK button.

Do not just press and release it.

Continue holding the button for more than one second.

Keep holding it until the Landroid’s red/blue exclamation-mark indicator becomes steady.

The important distinction is:

Rapidly flashing red/blue
        ≠
Correct pairing state

versus:

Steady red/blue exclamation indicator
        =
Pairing state

This was the key discovery that resolved the connectivity problem.

Procedure

1. Landroid is ON
2. Landroid is in charging station
3. Press OK
4. KEEP OK PRESSED
5. Wait until red/blue exclamation mark becomes STEADY
6. Release OK
7. Open/use Landroid app
8. Select Connect / Verbinden

The button must be held long enough to trigger the pairing state.

A short press is insufficient.

⸻

9. Pairing Through the Landroid App

With the Landroid showing the steady red/blue exclamation indicator, open the Landroid application.

Select:

Verbinden

or, in the English-language application:

Connect

The application then begins looking for the Landroid.

⸻

10. Be Patient During Discovery

The app may appear to be waiting for a relatively long time.

During the successful pairing attempt, the application displayed a Bluetooth-style icon with orange rings around it.

Although the exact underlying communication mechanism represented by this icon is not fully established, the icon is clearly part of the app’s local discovery/pairing sequence.

Do not assume that the process has failed simply because discovery takes a while.

Observed successful timing

The successful pairing took approximately:

~2 minutes

The application eventually recognized the Landroid S.

Therefore:

Wait rather than repeatedly restarting the pairing process.

The orange-ring discovery indication can remain visible for quite some time before the mower is recognized.

⸻

11. Confirm the Landroid

Once the application recognizes the mower:

1. Confirm the detected Landroid S.
2. Accept/confirm the pairing in the application.
3. Allow the application to complete the connection/configuration.

At this point the Landroid should be associated with the WiFi/network configuration.

⸻

12. Complete Successful Procedure

The complete working procedure can therefore be summarized as follows.

Network

Ziggo modem/router
       │
       │ Ethernet
       ▼
TP-Link Deco
metering cabinet
       │
       │ Deco mesh
       ▼
TP-Link Deco
garden
       │
       │ 2.4 GHz WiFi
       ▼
Landroid S
charging station

Pairing

Landroid in charging station
            │
            ▼
        Switch ON
            │
            ▼
       Hold OK > 1 sec
            │
            ▼
Red/blue exclamation becomes STEADY
            │
            ▼
Landroid app
"Verbinden" / "Connect"
            │
            ▼
Wait approximately 2 minutes
            │
            ▼
Landroid S recognized
            │
            ▼
           Confirm
            │
            ▼
           DONE

⸻

13. Troubleshooting

Landroid does not pair

First verify the physical setup:

* Landroid is actually in the charging station.
* Charging contacts are connected.
* Charging station shows its normal green light.
* Landroid is switched ON.
* The garden Deco is powered on.
* The garden Deco has a connection to the main Deco.
* The 2.4 GHz WiFi network is available at the charging station.

Then repeat the pairing sequence.

⸻

The exclamation mark is flashing rapidly

This is an important diagnostic indication.

Do not assume that the Landroid is ready to be discovered by the app.

Press and hold:

OK

for more than one second.

Continue holding it until the red/blue indicator becomes steady.

Then use:

Landroid app → Verbinden / Connect

⸻

The app appears to be searching for a long time

Wait.

The successful setup took approximately two minutes.

While waiting, the app displayed the Bluetooth-style discovery icon with orange rings.

Avoid immediately:

* restarting the mower,
* restarting the app,
* changing the WiFi configuration,
* moving the mower,
* repeatedly pressing OK.

Allow the discovery process to complete.

⸻

5 GHz WiFi is enabled

For initial troubleshooting/pairing, disable 5 GHz and provide the Landroid with a clearly available 2.4 GHz network.

This eliminates band-selection/compatibility issues from the pairing process.

⸻

WiFi signal is weak in the garden

Check the garden Deco.

The second Deco should be positioned so that it receives a reliable connection from the first Deco while also providing good coverage around the Landroid charging station.

Moving the garden Deco closer to the house or to a better position can improve the connection.

The goal is:

Deco #1  →  reliable mesh link  →  Deco #2
                                      │
                                      ▼
                                strong WiFi
                                      │
                                      ▼
                                  Landroid

⸻

14. What Ultimately Solved the Problem

Several possible causes were investigated, including:

* 2.4 GHz versus 5 GHz WiFi;
* garden WiFi coverage;
* TP-Link Deco configuration;
* WiFi configuration through USB;
* the Landroid’s charging state;
* the Landroid’s indicator lights;
* pairing through the mobile application.

The decisive solution was the OK-button pairing sequence.

The Landroid had to be placed in the charging station, powered on, and then the OK button had to be held down until the red/blue exclamation indicator changed from rapidly flashing to steady.

Only after reaching this state should Verbinden / Connect be pressed in the Landroid app.

The application then required approximately two minutes to discover the mower.

Once the Landroid S appeared, confirming it completed the setup.

⸻

15. Quick Reference

For future use, the entire procedure can be reduced to this checklist:

Network

* [ ]	Ziggo modem/router online
* [ ]	TP-Link Deco #1 connected by Ethernet in metering cabinet
* [ ]	TP-Link Deco #2 positioned in garden
* [ ]	Deco mesh connection working
* [ ]	Ziggo-<network>-extension available
* [ ]	2.4 GHz WiFi enabled
* [ ]	5 GHz disabled for initial pairing
* [ ]	Good WiFi signal at charging station

Landroid

* [ ]	Landroid physically in charging station
* [ ]	Charging contacts connected
* [ ]	Charging station green
* [ ]	Landroid switched ON
* [ ]	Hold OK for >1 second
* [ ]	Red/blue exclamation mark STEADY
* [ ]	Open Landroid app
* [ ]	Press Verbinden / Connect
* [ ]	Wait approximately 2 minutes
* [ ]	Wait for Landroid S to be recognized
* [ ]	Confirm
* [ ]	Done

⸻

16. Security Notes

Never commit the following to this repository:

* WiFi passwords
* Ziggo account credentials
* Landroid account credentials
* API tokens
* pairing tokens
* personal access tokens
* screenshots containing passwords or private credentials

Use placeholders such as:

Ziggo-<network>-extension

and:

<WIFI_PASSWORD>

when documenting configuration.

⸻

17. Lessons Learned

The most important lesson from this setup is that network connectivity and application pairing are two separate concerns.

A correctly configured 2.4 GHz WiFi network and good garden coverage are necessary, but they do not by themselves guarantee that the Landroid will be discovered by the app.

The mower must explicitly be placed into its pairing state.

The reliable sequence is:

Charging station → ON → hold OK → steady red/blue indicator → Connect in app → wait → confirm.

This should be treated as the canonical Landroid S pairing procedure for this installation.
