# How the pieces fit together

D-Modem's modem core is the centre of the suite. Everything else either
carries it somewhere or answers the calls it makes.

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

- **On a computer**, [D-Modem](https://github.com/D-Modem/D-Modem)'s
  `dmodemd` places a SIP call and gives the computer a serial port (a pty,
  a COM port or a socket). Terminal programs, fax software and `pppd` dial
  from it with AT commands, as they would a hardware modem.
- **On a phone**, the [D-Modem app](https://github.com/D-Modem/app) runs
  the same core on Android or iOS, with its own terminal, fax and dial-up
  internet.
- **On a real phone line**, a [pico-serial](https://github.com/D-Modem/hardware)
  Line stick is the line's interface, and D-Modem is the modem behind it.
  The serial adapters connect vintage computers to D-Modem as if it were
  a modem on their serial port.

## Answering

- **D-Modem's PBX modules** (`app_dmodem` for Asterisk and FreePBX,
  `mod_dmodem` for FreeSWITCH, `dmodem-ari`) answer a modem call on a
  phone number.
- **[modemmenu](https://github.com/D-Modem/menu)** is what the caller
  meets once the modems connect: a login, the message of the day and a
  menu of what they may do.
- **[bbs](https://github.com/D-Modem/bbs)** is one of those things: a
  bulletin board that also takes telnet, SSH and TN3270 callers, with
  [go3270](https://github.com/D-Modem/go3270) drawing its 3270 screens.

## Licences

Every repository is under the GNU AGPL 3.0 only, or a commercial licence
from the D-Modem Authors. go3270's code from upstream also keeps its MIT
licence. Each repository's README has the details.
