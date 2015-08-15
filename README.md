<a href="http://include-media.com">!['At' sign](http://include-media.com/assets/images/logo.png)</a>

# include-media — Grid plugin

> Get **include-media** [here](https://github.com/eduardoboucas/include-media).

### Introduction

This plugin generates classes for a grid system using [Harry Roberts' BEMIT naming convention](http://csswizardry.com/2015/08/bemit-taking-the-bem-naming-convention-a-step-further/), based on a number of subdivisions specified by the user, and taking into account all the breakpoints defined by **include-media**.

*Example:*

```scss
@import 'include-media';
@import 'include-media-make-grid';

$breakpoints: (
    'medium': 768px,
    'large': 1024px
);

// Dividing the layout in halves and thirds
@include im-grid(2, 3);
```

*Generates:*

```css
@media (min-width: 768px) {
  .col-1-2\@medium {
    width: 50%;
  }
  .col-2-2\@medium {
    width: 100%;
  }
  .col-1-3\@medium {
    width: 33.33333%;
  }
  .col-2-3\@medium {
    width: 66.66667%;
  }
  .col-3-3\@medium {
    width: 100%;
  }
}

@media (min-width: 1024px) {
  .col-1-2\@large {
    width: 50%;
  }
  .col-2-2\@large {
    width: 100%;
  }
  .col-1-3\@large {
    width: 33.33333%;
  }
  .col-2-3\@large {
    width: 66.66667%;
  }
  .col-3-3\@large {
    width: 100%;
  }
}
```

### Installation

- **Manually:** Download [this file](https://raw.githubusercontent.com/eduardoboucas/include-media-grid/master/_include-media-grid.scss) and import it into your Sass project
- **Bower:** Run `bower install include-media-grid`


### Usage examples

To create a grid where four elements in a row are displayed on the *large* view, two elements on the *medium* view and just one element on the *small* view, one can simply define the items as follows:

```scss
@include im-grid(1, 2, 4);
```

```html
<article class="col-1-4@large col-1-2@medium col-1-1@small"></article>
```
