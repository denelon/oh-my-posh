---
id: terraform
title: Terraform Context
sidebar_label: Terraform
---

## What

Display the currently active Terraform Workspace name.

:::caution
This requires a terraform binary in your PATH and will only show in directories that contain a `.terraform` subdirectory
:::

## Sample Configuration

```json
{
  "type": "terraform",
  "style": "powerline",
  "powerline_symbol": "\uE0B0",
  "foreground": "#000000",
  "background": "#ebcc34",
  "properties": {
    "template": "{{.WorkspaceName}}"
  },
}
```

## Properties

- fetch_version: `boolean` - fetch the version information from `versions.tf`, `main.tf` or `terraform.tfstate` -
defaults to `false`

## Template ([info][templates])

:::note default template

``` template
{{ .WorkspaceName }}{{ if .Version }} {{ .Version }}{{ end }}
```

:::

### Properties

- `.WorkspaceName`: `string` - is the current workspace name
- `.Version`: `string` - terraform version (set `fetch_version` to `true`)

[templates]: /docs/config-templates
