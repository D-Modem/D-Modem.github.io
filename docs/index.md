---
title: D-Modem
hide:
  - navigation
  - toc
---

<div class="suite-hero" markdown>
<img src="assets/suite/mark.svg" alt="">
<div markdown>

# D-Modem

**An open V.92 softmodem, and the app, boards and servers built around it.**

Dial a BBS, a fax machine or an ISP from a SIP call, a phone, or a real
phone line, without modem hardware. Or run the other end: answer modem
callers on a PBX, and give them a login, a menu and a bulletin board.

</div>
</div>

<div class="suite-home" markdown>

## The suite

<div class="grid cards" markdown>

-   **[D-Modem](https://github.com/D-Modem/D-Modem)**

    ---

    The softmodem: V.92 down to Bell 103, class 1, 2 and 2.0 fax, V.42 and
    V.44. `dmodemd` connects it to a SIP line. Modules put it in Asterisk,
    FreeSWITCH and FreePBX. It runs on Linux, Windows, macOS and Haiku.

-   **[app](https://github.com/D-Modem/app)**

    ---

    The D-Modem app for Android and iOS: a modem that uses a SIP call as
    its phone line. It has a terminal, a dialling directory, fax and
    dial-up internet.

-   **[hardware](https://github.com/D-Modem/hardware)**

    ---

    pico-serial: open RP2040 boards that connect D-Modem to vintage serial
    ports and to real telephone lines.

-   **[menu](https://github.com/D-Modem/menu)**

    ---

    modemmenu: the login and the menu that dial-up callers see first.
    Behind it, it can have PPP, a shell, the BBS or any other program.

-   **[bbs](https://github.com/D-Modem/bbs)**

    ---

    A bulletin board in Go for telnet, SSH, TN3270 and modem callers, with
    message areas, FidoNet, doors and file transfers.

-   **[go3270](https://github.com/D-Modem/go3270)**

    ---

    A Go library for TN3270 servers. It is the fork of racingmars/go3270
    for the suite. bbs uses it to draw its 3270 screens.

-   **[gui](https://github.com/D-Modem/gui)**

    ---

    Native desktop apps for D-Modem. We now develop them, and they are not
    complete. They will put the modem, its terminal and fax in a window on Windows,
    macOS and Linux.

-   **[brand](https://github.com/D-Modem/brand)**

    ---

    The mark, the Rainbow Book colours, type, the naming guide, and the
    theme that all D-Modem sites share.

</div>

## Start here

- **Dial from a computer:** build [D-Modem](https://github.com/D-Modem/D-Modem)
  and run `dmodemd` with a SIP account. Then dial from a terminal program.
- **Dial from a phone:** install the [D-Modem app](https://github.com/D-Modem/app).
- **Use a real phone line or serial port:** refer to the
  [pico-serial boards](https://github.com/D-Modem/hardware).
- **Answer callers:** put D-Modem in Asterisk. Then put
  [modemmenu](https://github.com/D-Modem/menu) and the
  [bbs](https://github.com/D-Modem/bbs) behind it.

[How the pieces fit together](suite.md){ .md-button }

</div>
