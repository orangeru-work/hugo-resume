# hugo-resume

A hugo module for displaying a data-driven, printable resume.

[🔗 demo site](https://hugo-resume.orangeru.work)

## features

* define resume data independently of presentation
* private fields not shown when HUGO_ENV is production
* page break will not happen within an experience item
* fairly high ATS compatibility
* print already configured for the important part of the page

## how to use

See the [exampleSite](./exampleSite/) directory for a working example.

Simply import the module in your hugo config file and add your resume data file containing your details to your site's data directory

## styles

`hugo-resume` supports multiple built-in styles located in `/static/css/styles/`:
* `default` (default for compatibility): classic serif style (Georgia font, blue block section headers)
* `stark`: modern slate & sky theme (system sans-serif fonts, clean underline section headers)

You can set the style via:
- **Page Frontmatter**: `style: stark` in your resume content file
- **Shortcode Argument**: `{{< resume style="stark" >}}`
- **Site Configuration**: `params.resumeStyle: stark` in your site configuration (`hugo.yml`)

## customization

Customization can be done by adding a css file at `/static/css/custom-resume.css` containing
changes to the classes defined in [resume.css](static/css/resume.css) or [stark.css](static/css/styles/stark.css)