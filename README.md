# DataverseGenerator

> A **console application** for generating Dataverse tables, fields, and relationships directly from a **Mermaid Entity Relation Diagram (ERD)**.

---

## ✨ Features

✅ **Generate Dataverse Tables, Columns, and Relations**

- Converts your Mermaid ERD into actual Dataverse tables.
- Creates basic field types including:
  - `int` (range: 0 – 1,000,000)
  - `datetime` (date only)
  - `decimal` (-1,000,000 to +1,000,000, precision 2)
  - `boolean` (true/1 or false/0)
  - `money` (-1,000,000 to +1,000,000, precision 2)

✅ **Supports One-to-Many Relations**

- Generates only one-to-many relationships.
- For many-to-many relationships, create your own **intersect tables** within your Mermaid ERD.

✅ **Common Data Model XML Reference**

- Requires an XML file containing **Common Data Model table names**.
- When referencing tables listed in this file, they will **not be prefixed**.
- Extend this file with your own tables (including prefixes) to use them seamlessly as lookup references in your ERD.

---

## 🔒 Security

Currently, the tool:

- Uses the **default AppId**.
- Authenticates and authorises using your **user account**.

---

## 🚀 Usage

1. **Download** the executable, the XML reference file, and prepare your own Mermaid (.mmd) file.

2. **Run the tool** with the following command:

```bash
dataversegenerator.exe <url> <mmd-file> <prefix> [--dry-run] [--solution Name] [--log-level Level] [--log-file Path] [--log-json]
```

| Argument            | Description                                                         |
| ------------------- | ------------------------------------------------------------------- |
| `<url>`             | Dataverse environment URL                                           |
| `<mmd-file>`        | Path to your Mermaid ER diagram file                                |
| `<prefix>`          | Prefix for newly created tables                                     |
| `--dry-run`         | *(Optional)* Shows what would be generated without applying changes |
| `--solution Name`   | *(Optional)* Target solution for creation                           |
| `--log-level Level` | *(Optional)* Sets logging level (e.g. info, debug)                  |
| `--log-file Path`   | *(Optional)* Outputs logs to a specified file                       |
| `--log-json`        | *(Optional)* Outputs logs in JSON format                            |

## 💡 Notes

Ensure your Mermaid diagram syntax is valid and aligned with the supported field types and relationships.

For many-to-many relations, manually define intersect tables within your ERD.

---

## 🔭 Roadmap

Planned features include:
- Support for additional field types.
- Many-to-many relationship generation.
- Multiple authentication methods for Dataverse connection.
- XRMToolbox plugin

