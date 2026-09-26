# dbt-init Instructions

`core/` generates the dbt starter project in `starter-project/`; change templates and generator logic together so placeholders and resulting files stay aligned. Create a Python 3 virtual environment and install the documented development dependencies with `pip install -r requirements-dev.txt`.

For a generator change, run `dbt-init --client test --target-dir <temporary-directory> --warehouse bigquery`, then inspect the new `test-dbt` directory. This creates files locally but does not validate a warehouse connection; `dbt debug` and `dbt run` require a configured profile and real credentials. Generated profiles must remain credential-free, and no customer target directory belongs in routine validation.
