---
id: version-4.5.0-webui
title: Web User Interface
original_id: webui
---

![Uplinks](https://user-images.githubusercontent.com/558752/52916111-fa4ba980-32db-11e9-8a64-f4e06eb920b3.png)

<div id="codefund">''</div>

Verdaccio has a web user interface to display only the private packages and can be customisable.

```yaml
web:
  enable: true
  title: Verdaccio
  logo: logo.png
  primary_color: "#4b5e40"
  gravatar: true | false
  scope: "@scope"
  sort_packages: asc | desc
```

All access restrictions defined to [protect your packages](protect-your-dependencies.md) will also apply to the Web Interface.

### Internationalization

*Since v4.5.0*, there are translations available

```yaml
i18n:
  web: en-US  
```

> ⚠️ Only the languages in this [list](https://github.com/verdaccio/ui/tree/master/i18n/translations) are available, feel free to contribute with more. The default one is es-US

### Konfiguracja

| Właściwość    | Typ         | Wymagane | Przykład                                                      | Wsparcie   | Opis                                                                                                                     |
| ------------- | ----------- | -------- | ------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------ |
| enable        | boolean     | Nie      | true/false                                                    | wszystkie  | allow to display the web interface                                                                                       |
| title         | ciąg znaków | Nie      | Verdaccio                                                     | wszystkie  | HTML head title description                                                                                              |
| gravatar      | boolean     | Nie      | true                                                          | `>v4`   | Gravatars will be generated under the hood if this property is enabled                                                   |
| sort_packages | [asc,desc]  | Nie      | asc                                                           | `>v4`   | By default private packages are sorted by ascending                                                                      |
| logo          | ciąg znaków | Nie      | `/local/path/to/my/logo.png` `http://my.logo.domain/logo.png` | wszystkie  | a URI where logo is located (header logo)                                                                                |
| primary_color | ciąg znaków | Nie      | "#4b5e40"                                                     | `>4`    | The primary color to use throughout the UI (header, etc)                                                                 |
| scope         | ciąg znaków | Nie      | @myscope                                                      | `>v3.x` | If you're using this registry for a specific module scope, specify that scope to set it in the webui instructions header |


> It is recommended the logo size has the following size `40x40` pixels.
