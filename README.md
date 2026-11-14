# D-Modem.github.io

This is the website of the D-Modem suite, <https://d-modem.github.io/>.
It tells what the suite is, and gives the location of the site of each
repository in the suite.

The pages are in `docs/`. Zensical builds them with the shared theme from
[brand](https://github.com/D-Modem/brand) (refer to its
[docs/sites.md](https://github.com/D-Modem/brand/blob/main/docs/sites.md)).
`.github/workflows/pages.yml` deploys them on each push to main.

To preview the site, clone brand next to this repository. Then run these
commands:

    pip install -r ../brand/pages/requirements.txt
    ../brand/tools/site.sh . serve

## Licence

AGPL-3.0-only ([LICENSE](LICENSE)), or a commercial licence from the D-Modem Authors ([COMMERCIAL-LICENSE.md](COMMERCIAL-LICENSE.md)). Contributions come with a contributor agreement ([CONTRIBUTING.md](CONTRIBUTING.md)).
