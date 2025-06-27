# DataverseGenerator
A console application for generating Dataverse tables, field and relations from a Mermaid Entity Relation Diagram


## Features

A Console application for generating Dataverse Tables, Columns and Relations between tables al from the input of a Mermaid ERDiagram.
This tool can for now create some basic fields like:
- int, 
- datetime (dateonly)
- decimal (-1000000 - 1000000, precision 2)
- boolean (true/1 or false/0)
- money (-1000000 - 1000000, precision 2)
Also the tool only create one-to-many relations, so if you need many-to-many relations you should create your own intersect table in the ERDiagram.
There is a second file needed for running the tool, this one you are able to expand yourself. This file contains the Common Datamodel tablenames, so if you reference one of these table it will not prefix thes.
With this file you are also able to add your own tables, with prefixes allready applied if you're creating lookups to these tables.

## Security

This tool uses the default AppId for now, aswell as using your user account for the authentication and authorisation. In later updates expect multiple ways of connecting to Dataverse.

## Usage

To run the tool download the executable, XML and provide your own MMD file.

Next run the following command: dataversegenerator.exe <url> <mmd-file> <prefix> [--dry-run] [--solution Name] [--log-level Level] [--log-file Path] [--log-json]
