[English](Getting-Started) · **Dansk** · [Bahasa Melayu](Getting-Started-ms)

# Kom godt i gang

## Krav

Python 3.13 eller nyere og `pytest` til testene. Der er ingen afhængigheder ved kørsel. For at køre testene og kodekontrollerne installerer du udviklingsværktøjerne med `python -m pip install -e ".[dev]"`.

## Opsætning

```bash
python -m venv .venv
source .venv/bin/activate        # Windows PowerShell: .\.venv\Scripts\Activate.ps1
python -m pip install -e ".[dev]"
```

## Kør

```bash
python -m coffee_machine
```

## Tests

```bash
python -m pytest
```

## Licens

Koden er udgivet under licensen the GNU Affero General Public License v3.0 or later (AGPL-3.0-or-later). Se filen `LICENSE`.
