# Signal Sciences Rule Cloner Script

This repository contains two Python scripts that facilitate the cloning of rules and rate limit rules within the Signal Sciences dashboard from one site to another.
This is as-is and not an official feature of the product, therefore there is no support. 

USE AT YOUR OWN RISK!

## Prerequisites

Before you begin, ensure you have the following:

- Python 3.x installed on your system.
- The `requests` library installed in Python. You can install it with `pip install requests`.
- Your Signal Sciences API credentials (API user and API token).

## Installation

Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/yourusername/signalsciences-rule-cloner.git
cd signalsciences-rule-cloner
```
## Usage
The scripts require Signal Sciences API credentials and the IDs of the source and destination sites to function correctly.

## List existing rules

```bash
python3 rule_cloner.py <api_user> <api_token> <corp> --source_site <source_site_id> --destination_site <destination_site_id> --show_rules
# example 
python3 rule_cloner.py user@example.com 12345-abcdefg-000-fffff --source_site staging --destination_site production --show_rules
```


## Copying a Single Rule
To copy a single rule from one site to another, you can run rule_cloner.py with the --rule_id argument to specify which rule to copy.

```bash
python3 rule_cloner.py <api_user> <api_token> <corp> --source_site <source_site_id> --destination_site <destination_site_id> --rule_id <rule_id>
# example
python3 rule_cloner.py user@example.com 12345-abcdefg-000-fffff --source_site staging --destination_site production --rule_id 699effd2lop3daf55

```

## Copying all rules

```bash
python3 rule_cloner.py <api_user> <api_token> <corp> --source_site <source_site_id> --destination_site <destination_site_id>
# example
python3 rule_cloner.py user@example.com 12345-abcdefg-000-fffff --source_site staging --destination_site production