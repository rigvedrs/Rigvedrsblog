---
title: "Firstpost"
date: 2022-06-21T17:57:07+05:30
draft: true
---

For referencing syntax and testing


## Outputing image

{{< figure src="/firstblog/RollsRoyce.jpg" title="Rolls (figure)" >}}


## Printing gist

{{< gist spf13 7896402 >}}



## Highlighting HTML

{{< highlight html >}}
<section id="main">
    <div>
        <h1 id="title">{{ .Title }}</h1>
        {{ range .Pages }}
            {{ .Render "summary"}}
        {{ end }}
    </div>
</section>
{{< /highlight >}}


## For Code
```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
