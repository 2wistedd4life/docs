---
title: Creating and highlighting code blocks
intro: Share samples of code with fenced code blocks and enabling syntax highlighting.
redirect_from:
  - /articles/creating-and-highlighting-code-blocks
  - /github/writing-on-github/creating-and-highlighting-code-blocks
  - /github/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
shortTitle: Create code blocks
---

## Fenced code blocks

You can create fenced code blocks by placing triple backticks <code>\`\`\`</code> before and after the code block. We recommend placing a blank line before and after code blocks to make the raw formatting easier to read.

<pre>
```
function test() {
  console.log("notice the blank line before this function?");
}
```
</pre>

![Rendered fenced code block](/assets/images/help/writing/fenced-code-block-rendered.png)

{% tip %}

**Tip:** To preserve your formatting within a list, make sure to indent non-fenced code blocks by eight spaces.

{% endtip %}

To display triple backticks in a fenced code block, wrap them inside quadruple backticks.


<pre>
````
```
Look! You can see my backticks.
```
````
</pre>

![Rendered fenced code with backticks block](/assets/images/help/writing/fenced-code-show-backticks-rendered.png)

{% data reusables.user-settings.enabling-fixed-width-fonts %}

## Syntax highlighting

<!-- If you make changes to this feature, check whether any of the changes affect languages listed in /get-started/learning-about-github/github-language-support. If so, please update the language support article accordingly. -->

You can add an optional language identifier to enable syntax highlighting in your fenced code block.

For example, to syntax highlight Ruby code:

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```

![Rendered code block with Ruby syntax highlighting](/assets/images/help/writing/code-block-syntax-highlighting-rendered.png)

We use [Linguist](https://github.com/github/linguist) to perform language detection and to select [third-party grammars](https://github.com/github/linguist/blob/master/vendor/README.md) for syntax highlighting. You can find out which keywords are valid in [the languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

{% ifversion mermaid %}
## Creating diagrams

You can also use code blocks to create diagrams in Markdown. GitHub supports Mermaid, GeoJSON, TopoJSON, and ASCII STL syntax. For more information, see "[Creating diagrams](/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams)."

{% endif %}
## Further reading

- [{% data variables.product.prodname_dotcom %} Flavored Markdown Spec](https://github.github.com/gfm/)
- "[Basic writing and formatting syntax](/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)"
