# Local installation and first analysis

Applies to **authorized copies** of v0.5.0 and v0.4.2-fix3. The public repository currently contains no application download or runnable backend. Cloning it is not an installation step for the platform.

## Requirements

| Requirement | v0.5.0 | v0.4.2-fix3 Demo |
| --- | --- | --- |
| Python installed by the user | 3.12 or newer, subject to dependency availability | 3.12.x for the Windows setup script |
| Included frontend | Built frontend included | Built frontend included |
| Python / virtual environment bundled | No | No |
| Node.js for ordinary use | Not required | Not required |
| First setup | Internet access to install dependencies | Internet access to install dependencies |
| Launch URL | http://127.0.0.1:8000 | http://127.0.0.1:8000 |

Extract to a writable directory. Keep the Demo and current version in separate program directories. A minimum-Python check is not a guarantee that all newer versions have compatible dependency wheels.

## Windows

1. Install the appropriate Python version, then extract the full application archive.
2. Open `setup.bat` in the application directory to create the project `.venv` and install dependencies. v0.5.0 also performs environment diagnostics.
3. Optionally copy `.env.example` to `.env` and configure your own model provider. Without a model you can still run analysis and generate factual reports.
4. Open `start.bat`, then visit http://127.0.0.1:8000 and create a local account.

v0.5.0 can select an installed interpreter explicitly:

```bat
setup.bat --python "C:\Path\To\Python\python.exe"
```

Its launcher uses the project environment. Setup does not install Python, edit system PATH or silently delete an existing invalid `.venv`. Follow its message to rename that environment before changing Python minor versions.

## Linux / macOS entry points in v0.5.0

After installing Python 3.12+, run these commands from the extracted application directory:

```sh
bash setup.sh
# Optionally copy .env.example to .env and configure your provider.
bash start.sh
```

Use `bash setup.sh --python /path/to/python` to choose an interpreter. Linux verification is limited to the recorded environments; native macOS verification remains unestablished. These shell commands are not Demo Windows instructions.

## First analysis

1. Describe the experiment in the welcome workspace, select **P2** or **G2**, and confirm task creation.
2. In **Inputs**, upload the required tables. P2 needs protein reporter CSV. G2 needs protein reporter CSV, enriched peptide reporter CSV and matching UniProt FASTA.
3. Check experimental design and map sample conditions explicitly. P2 requires a Vehicle and treatment; G2 requires exactly one protein sample named `control`, with protein and peptide mappings handled separately.
4. Confirm three matched biological replicate pairs: **129/126, 130/127, 131/128**. Unsupported replicate designs require clarification, not forced mapping.
5. Save parameters, use **Validate inputs & mapping**, then **Review this run**. Inspect the design, configuration and input identity before **Confirm & run**. Changing inputs or parameters requires another review.
6. In **Results**, select the desired run and inspect QC, tables, figures and the factual report. Model interpretation is optional and requires scientific review.
7. Wait for analysis, figure and report jobs to finish before downloading the complete archive. A standalone HTML report may depend on separate image files; use the full archive for offline viewing.

## Optional model configuration

Use the instructions and `.env.example` supplied with your specific package. Model mode requires `REFINEDTPP_ENABLE_LLM=1` plus the provider URL, model and your own key. Do not commit `.env` or include it in public diagnostics.

After editing configuration, open **Learn → Model configuration**, reload it and test the connection. Automatic model interpretation is off by default. Enabling model mode sends relevant context/evidence to the provider and can consume its API quota; local analysis does not require it.

## Upgrade and backup

1. Stop the old service and ensure no analysis is active.
2. Back up the complete old application and its entire data directory, plus `.env`.
3. Extract v0.5.0 into a separate directory. Copy `.env` and the full old data directory if retaining tasks; do not copy the old `.venv`.
4. Run the newer setup/start scripts. v0.5.0 checks the database schema and backs up SQLite before migration. Check login, tasks and a historical run.
5. Regenerate a report to obtain new reporting fields and begin snapshot history; that alone does not require rerunning statistics.

`backup.bat` / `bash backup.sh` in v0.5.0 backs up **SQLite only**. Complete scientific backup requires stopping the service and copying the whole data directory, including uploads, frozen inputs, results, figures and reports. Never let both versions write to the same data directory. Rollback uses the pre-upgrade copy, not the migrated database.

## Troubleshooting

v0.5.0 provides `check_environment.bat` / `bash check_environment.sh`. Interrupted scientific analyses require a new run; supported figure/report jobs can be retried separately. There is no arbitrary-stage scientific resume.

For public bug reports, identify the exact version, OS, Python version and package source, and share a synthetic reproduction with redacted logs. See [security reporting](../SECURITY.md) for vulnerabilities.
