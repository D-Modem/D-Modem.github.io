# How the pieces fit together

The modem core of D-Modem is the centre of the suite. Each other part of
the suite either carries the core to a different location or answers the
calls that it makes.

```
 caller's side                               answering side
 ─────────────                               ──────────────
 terminal, fax, PPP                          Asterisk / FreeSWITCH / FreePBX
        │                                               │
 dmodemd (D-Modem)  ── SIP call ──▶  PBX ──▶  app_dmodem (D-Modem)
   or the app                                           │
   or a pico-serial stick on a phone line          modemmenu (menu)
                                                        │
                                                bbs, PPP, a shell
```

## Calling out

- **On a computer**, `dmodemd` of [D-Modem](https://github.com/D-Modem/D-Modem)
  makes a SIP call and gives the computer a serial port (a pty, a COM
  port or a socket). Terminal programs, fax software and `pppd` dial
  through this port with AT commands, as with a hardware modem.
- **On a phone**, the [D-Modem app](https://github.com/D-Modem/app) runs
  the same core on Android or iOS, with its own terminal, fax and dial-up
  internet.
- **On a real phone line**, a [pico-serial](https://github.com/D-Modem/hardware)
  Line stick is the interface to the line, and D-Modem is the modem
  behind it. The serial adapters connect vintage computers to D-Modem.
  To the computer, D-Modem is the same as a modem on its serial port.

## Answering

- **The PBX modules of D-Modem** (`app_dmodem` for Asterisk and FreePBX,
  `mod_dmodem` for FreeSWITCH, `dmodem-ari`) answer a modem call on a
  phone number.
- **[modemmenu](https://github.com/D-Modem/menu)** is the first thing
  that the caller sees when the modems connect. It gives a login, the
  message of the day and a menu of the tasks that the caller can do.
- **[bbs](https://github.com/D-Modem/bbs)** is one of those tasks. It is
  a bulletin board that also accepts telnet, SSH and TN3270 callers.
  [go3270](https://github.com/D-Modem/go3270) draws its 3270 screens.

## Licences

Each repository is under the GNU AGPL 3.0 only, or a commercial licence
from the D-Modem Authors. The upstream code of go3270 also keeps its MIT
licence. The README of each repository has the details.
