# Security

## Reporting a vulnerability

Email **mustafasameen@ufl.edu**. Do not open a public issue for a security report.

## What counts here

HDSim is a research library. The risks worth reporting are about what it does with your credentials
and your data:

- **Credential handling.** `HDSIM_API_KEY` is read from the environment or a `.env` file. A path
  where a key is logged, written to disk, or sent anywhere other than the configured `HDSIM_BASE_URL`
  is a vulnerability. Report it.
- **Data exfiltration.** The library sends persona text to whatever endpoint you configure. A path
  that sends survey records somewhere you did not configure is a vulnerability.
- **Code execution.** Loading a household file or a survey extract must never execute code from it.

## What does not count

- A model returning a wrong or biased decision. That is a research limitation, not a vulnerability;
  open a normal issue.
- Cost incurred by running a live simulation against a paid endpoint.

## Supported versions

The project is pre-1.0. Fixes land on `main`; there is no backport branch yet.
