# Clair Scan Action

This action executes clair scanning by using the official clair Docker image and
restricted only to a given `updater`

## Inputs

## `updater`

**Required**: The updater name for scanning as specified in the
[Clair config documentation](https://github.com/quay/clair/blob/main/Documentation/reference/config.md#updaterssets)

E.g.: `debian`

## `image`

**Required**: Container image to analyze.

E.g.: vulnerables/web-dvwa

## `report_path`

**Required**: Path to save the report

E.g.: `clairReport.json`

## `report_format`

**Optional**: Report format. Values: xml | json | text

**Default value**: `json`

E.g.: `json`

## Example usage

    - name: Clair Scan
      uses: santander-group/clair-scan-action@main
      with:
        updater: debian
        image: vulnerables/web-dvwa
        report_path: clair-report.json
        report_format: json

## Getting involved

This project is far from being perfect, so any help is always welcome. Please,
review our [CONTRIBUTING](CONTRIBUTING.md) file to know how to get involved.

---

## Licensing info

* [LICENSE](LICENSE)

---

## Credits and references

1. [Clair](https://github.com/quay/clair)
2. [Creating actions official documentation](https://docs.github.com/en/actions/creating-actions)
