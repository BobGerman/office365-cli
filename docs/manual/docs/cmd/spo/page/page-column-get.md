# spo page column get

Get information about a specific column of a modern page

## Usage

```sh
spo page column get [options]
```

## Options

Option|Description
------|-----------
`--help`|output usage information
`-u, --webUrl <webUrl>`|URL of the site where the page to retrieve is located
`-n, --name <name>`|Name of the page to get column information of
`-s, --section <section>`|ID of the section where the column is located
`-c, --column <column>`|ID of the column for which to retrieve more information
`-o, --output [output]`|Output type. `json|text`. Default `text`
`--verbose`|Runs command with verbose logging
`--debug`|Runs command with debug logging

!!! important
    Before using this command, log in to a SharePoint Online site, using the [spo login](../login.md) command.

## Remarks

To get information about the specific column of a modern page, you have to first log in to a SharePoint site using the [spo login](../login.md) command, eg. `spo login https://contoso.sharepoint.com`.

If the specified name doesn't refer to an existing modern page, you will get a _File doesn't exists_ error.

## Examples

Get information about the first column in the first section of a modern page with name _home.aspx_

```sh
spo page column get --webUrl https://contoso.sharepoint.com/sites/team-a --name home.aspx --section 1 --column 1
```