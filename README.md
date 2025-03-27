# Greg Smith Design

## Credit

Using [jekyll-tachyons](https://github.com/leonp/jekyll-tachyons) by [Leon Paternoster](https://www.leonpaternoster.com).

## Jekyll Tachyons

Follow the jekyll-tachyons link above for full README. Shortened README included below.

## Installation

1. install [Bundler](http://bundler.io/)
2. navigate to the theme folder
3. run `bundle update`
4. run `bundle install`
5. run `bundle exec jekyll s` to serve and build the site

## Working locally

TE = TextExpander Snippet

1. TE: `jekbuild` Result: `bundle exec jekyll build`
2. TE: `jekclean` Result: `bundle exec jekyll clean`
3. TE: `jekserve` Result: `bundle exec jekyll serve -l`

## Inlining styles in the head

Include this line in `_config.yml`:

`css: inline`

Otherwise, the theme will link to a separate CSS file (`/css/style.css`). This is the default behavior.

## Selecting Tachyons modules

Comment out any modules you don't want to include:

`// "negative-margins"`

- If you're inlining styles, edit the list in `/_includes/style.scss`
- If you're referring to an external stylesheet, edit the list in `/css/style.scss`

There are 2 additional SASS files:

- `_c.scss` - additional user styles
- `_variables.scss` - variables you want to refer to in `_c.scss`

Alternatively, import just the following files. You can comment out or even delete the rest.

1. `_tachyons-4.8.1.scss`
2. `_variables.scss`
3. `_c.scss`

If you haven't created custom variables and/or rules, you only need to import `_tachyons-4.8.1.scss`.

## Media queries

Tachyons is mobile first.

- `db` (default, applies to all screen widths)
- `db-ns` (applies to medium and large screen widths)
- `db-m` (applies to medium screen widths only)
- `db-l` (applies to large screen widths and up only)

These lines define your responsive breakpoint defaults:

`
$breakpoint-not-small: 'screen and (min-width: 30em)' !default;
$breakpoint-medium: 'screen and (min-width: 30em) and (max-width: 60em)' !default;
$breakpoint-large: 'screen and (min-width: 60em)' !default;
`

Comment out or delete these lines and replace them with your new screen width ranges. For example:

`
$breakpoint-not-small: 'screen and (min-width: 40em)' !default;
$breakpoint-medium: 'screen and (min-width: 40em) and (max-width: 64em)' !default;
$breakpoint-large: 'screen and (min-width: 64em)' !default;
`

Now, your responsive suffixes will work like so:

- `db` (default, applies to all screen widths)
- `db-ns` (applies to 40em screen widths and up)
- `db-m` (applies to medium screen widths only, i.e. between 40em and 64em)
- `db-l` (applies to large screen widths and up only, i.e. 64em and up)

## Import Order

Because the SASS files refer to each other and `_c.scss` may refer to `_variables.scss`, the first files you import should be:

1. `_normalize.scss`
2. `_media-queries.scss`
3. `_variables.scss`
4. `_colors.scss`
5. `_spacing.scss`
