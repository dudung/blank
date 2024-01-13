+++
title = 'Curved line with SVG path'
date = 2024-01-13T05:08:59+07:00
draft = false
+++
Draw curved line using [path](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths) element in [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG).


## create post
```
D:\blank>hugo new content tests\curved-line-with-svg-path.md
Content "D:\\blank\\content\\tests\\curved-line-with-svg-path.md" created
```

Put it in `tests` folder first while re-develop `svgpath.html` from `layouts\shortcodes` in `plaintext` to `layouts\shortcodes\blank`.


## test 1
{{< blank/svgpath >}}
B_STYLE red,3,#ccf
M 50 50 l 100 0
v 100 h -100 z
{{< /blank/svgpath >}}


## test 2
{{< blank/svgpath >}}
B_STYLE #f44,3,#fcc
M 150 100 l 50 0 l 0 -50 l -100 0 l 0 100 l 100 0 m 0 -25
m -25 0 l -50 0 l 0 -50 l 50 0
{{< /blank/svgpath >}}

