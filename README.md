# Hugo Favicon

Add the favicons generated from [RealFaviconGenerator](https://realfavicongenerator.net/) to your website.
Hugo Favicon will generate the `site.webmanifest` file.

## Usage

1) Generate the favicons and download from https://realfavicongenerator.net/.
2) Move the **image files** to `assets/images`.
3) Add `{{ partial "head/favicons.html" . }}` to the `<head>` element.

## Configuration

```toml
[params]
  [params.favicon]
    theme       = "#ffffff" # Defaults to #ffffff
    background  = "#ffffff" # Defaults to #ffffff
    [params.favicon.webmanifest]
      fingerprint   = false # Fingerprint the URL for the webmanifest file
      title       = "My Site" # Defaults to site.Title if not present
      shortTitle  = "Site"    # Defaults to site.Params.shortTitle, site.Params.favicon.webmanifest.title, or site.Title
```