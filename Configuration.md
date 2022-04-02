This page contains the below configuration.
- [Font](#Font)
- [Color palette](#Color-palette)
- [Theme](#Theme)
- [SEO](#SEO)
- [Navbar](#Navbar)
- [Footer](#Footer)
- [Custom CSS](#Custom-CSS)
- [SubPath to serve static files](#SubPath-to-serve-static-files)

See the [configurations](https://github.com/gurusabarish/hugo-profile/wiki/Pages-or-Sections) for pages or sections.

# Font
You can customize the font size, font weight, line height, text align properties in `config.yaml`

```yaml
params:
    font:
        fontSize: 1.5rem # default: 1rem
        fontWeight: 500 # default: 400
        lineHeight: 1 # default: 1.5
        textAlign: right # default: left
```

**Font used**
- [Roboto](https://fonts.google.com/specimen/Roboto)
- [Alata](https://fonts.google.com/specimen/Alata)
- [Lara](https://fonts.google.com/specimen/Lora)

If you want to customize the font, edit these files [head.html]('./../../layouts/partials/head.html'), [font.css]('./../../static/css/font.css')

# Color palette
You can customize the color palette in `config.yaml`. For [more details](https://github.com/gurusabarish/hugo-profile/wiki/Color-Customization)

```yaml
params:
  color:
    textColor: <value>
    secondaryTextColor: <value>
    backgroundColor: <value>
    secondaryBackgroundColor: <value> 
    primaryColor: <value>
    secondaryColor: <value>

    darkmode:
      textColor: <value>
      secondaryTextColor: <value>
      backgroundColor: <value>
      secondaryBackgroundColor: <value>
      primaryColor: <value>
      secondaryColor: <value>
```

# Theme
you can disable the toggle in `config.yaml`. It will be in auto by default.

```yaml
params:
    theme:
        disableThemeToggle: false
        defaultTheme: "light" # or dark
```

# SEO

It has Hugo's [`_internal/opengraph.html`](https://gohugo.io/templates/internal/#open-graph), [`_internal/twitter_cards.html`](https://gohugo.io/templates/internal/#twitter-cards).
- [How to use opengraph](https://gohugo.io/templates/internal/#open-graph)
- [How to use twitter cards](https://gohugo.io/templates/internal/#twitter-cards)

# Navbar
If you want to customize the menu, you can customize in `config.yaml`
- alignment: It will align the menus. If you didn't specify by default it will be `ms-auto`. *Left: `ms-auto` | center: `mx-auto` | right: `me-auto`*.
- brandLogo: If you want you different logo for brand, you can change by this property.
- brandName: If you want you different name for brand, you can change by this property.

```yaml
params:
    navbar:
        align: mx-auto
        brandLogo: "/logo.png" # Logo for the brand | default is the favicon variable
        brandName: "Profile" # Brand name for the brand | default is the title variable
```

## Menus
It follows Hugo's [menus](https://gohugo.io/content-management/menus)

```yaml
Menus:
  main:
    - identifier: blog
      name: Blog
      title: Blog posts
      url: /blog
      weight: 1

    #Dropdown menu
    - identifier: dropdown
      title: Example dropdown menu
      name: Dropdown
      weight: 2
    - identifier: dropdown1
      title: example dropdown 1
      name: example 1
      url: /#
      parent: dropdown
      weight: 1
    - identifier: dropdown2
      title: example dropdown 2
      name: example 2
      url: /#
      parent: dropdown
      weight: 2
```

# Footer
```yaml
footer:
    # recentPosts: false
    socialNetworks:
      github: https://github.com
      linkedin: https://linkedin.com
      twitter: https://twitter.com
      instagram: https://instagram.com
      facebook: https://facebook.com
```

# Custom CSS
- If you want to use custom styling, then create a file named `style.css` inside static folder
- Before adding your styles into the file, enable the customCSS configuartion in `config.yaml`.
```yaml
params:
  customCSS: true
```

# SubPath to serve static files
To allow websites in a sub-path like `<ghuser-or-org>.github.io/myhugosite/`
```yaml
params:
  staticPath: "/your/path/"
```