# D-Modem.github.io

The D-Modem suite's website, <https://d-modem.github.io/>: what the
suite is and where each of its repositories' sites lives.

The pages are under `docs/`. They're built with MkDocs and the shared
theme from [brand](https://github.com/D-Modem/brand) (its
[docs/sites.md](https://github.com/D-Modem/brand/blob/main/docs/sites.md)),
and deployed by `.github/workflows/pages.yml` on every push to main.

To preview, with brand cloned beside this repository:

    pip install -r ../brand/pages/requirements.txt
    ../brand/tools/site.sh . serve

