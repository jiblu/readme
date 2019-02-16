## 3. Templates

If you have come this far you are probably interested to figure out how to use readme templates. This library comes with a set of pre-defined templates to make your readme awesome, but you can of course create your own. More about that later, let's not get ahead of our self just yet.

The most simple template you can use is the title template. The way to generate a title is by writing `{{ template:title }}` in your blueprint. When you run the `readme` command the template will generate the following:

[[ template:title ]]

The important thing to note here is that the template automatically reads your `package.json` file and inserts the `name` from the package. That's pretty cool. Let's go through some of the other built-in templates you might want to add.

### Logo

The logo template adds a logo to your readme and looks like this:

[[ template:logo ]]

Use the placeholder `{{ template:logo }}` to stamp it. You will need to add the `readme.logo` field to your `package.json`. The logo field requires an `url` field and the fields `width`, `height` and `alt` are optional. Below is an example on how to add a logo.

```json
{
  "readme": {
    "logo": {
      "url": "https://avatars1.githubusercontent.com/u/6267397?s=460&v=4",
      "width": 100
    }
  }
}
```


### Badges

The badges template adds badges to your readme and looks like this:

[[ template:badges ]]

Use the `{{ template:badges }}` placeholder to stamp it. You will need to add the information about how the badges should be generated. For that you can extend the "readme.ids" property in your `package.json` add the `npm` and `github` ids (both are optional). If you want to add your own badges you can use the `readme.badges` field.

```json
{
  "readme": {
    "ids": {
      "github": "andreasbm/readme",
      "npm": "@appnest/readme"
    },
    "badges": [
      {
        "alt": "Custom badge",
        "url": "https://github.com/badges/shields",
        "img": "https://img.shields.io/badge/custom-badge-f39f37.svg"
      }
    ]
  }
}
```

### Description

The description template adds a description to your readme and looks like this:

[[ template:description ]]

Use the `{{ template:description }}` placeholder to stamp it. To use this template you are required to add the field `description` to your `package.json` file. Optionally you can also add the fields `readme.text` and `readme.demo` which will be presented below the description.

```json
{
  "description": "Generate pretty README.md files with your new superpowers!",
  "readme": {
    "text": "Use this readme generator to easily generate pretty readme's like this one! Simply extend your <code>package.json</code> and create a readme blueprint.",
    "demo": "https://my-demo-url.com"
  }
}
```

### Bullets

The bullets template adds bullets to your readme and looks like this:

[[ template:bullets ]]

Use the `{{ template:bullets }}` placeholder to stamp it. To use this template you are required to add the `readme.bullets` array to your `package.json` file. This array has to be an array of strings as shown below.

```json
{
  "description": "Generate pretty README.md files with your new superpowers!",
  "readme": {
    "bullets": [
      "**Simple:** Extremely simple to use - so simple that it almost feels like magic!",
      "**Powerful:** Customize almost everything - add your own templates and variables if you like",
      "**Awesome:** The tool you don't know you need before you have many different repositories that all need maintanence"
    ]
  }
}
```

### Table of Contents

The table of contents template adds a table of contents and looks like this:

[[ template:toc ]]

Use the `{{ template:toc }}` placeholder to stamp it. It has been scientifically proven that this template will save you approximately 392.3 hours during your life-time.

### Contributors

The contributors template adds the list of contributors and looks like this:

[[ template:contributors ]]

Use the `{{ template:contributors }}` placeholder to stamp it. To use this template your are required to add the `contributors` array to your `package.json` file like this.

```json
{
  "contributors": [
    {
      "name": "Andreas Mehlsen",
      "email": "andmehlsen@gmail.com",
      "url": "https://twitter.com/andreasmehlsen"
    }
  ]
}
```

### License

The license template adds a license section and looks like this:

[[ template:license ]]

Use the `{{ template:license }}` placeholder to stamp it. To use this template you are required to add the `license` field to your `package.json` file like this.

```json
{
  "license": "MIT"
}
```