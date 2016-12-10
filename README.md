# Hamburger Icon

> A collection of mixins for creating hamburger icons.

Basic idea — [Sass Burger](https://github.com/jorenvanhee/sass-burger).

## Support

Support for all popular css preprocessors: [Less](http://lesscss.org/), [Sass](http://sass-lang.com/) and [Stylus](http://learnboost.github.io/stylus/).

## Installation

* Download the files you need from the this repository;
* Bower: `$ bower install hamburger-icon --save`;
* Git: `$ git clone git://github.com/mrmlnc/hamburger-icon.git`;

Then just import the file, whitch includes variables colors in your project.

**Less:**

````Less
  @import "lib/hamburger-icon";
````

**Sass:**

````Sass
  @import "lib/hamburger-icon"
````

**Stylus:**

````Stylus
  @import "lib/hamburger-icon"
````

If you use Bower, the path would be:

````
  bower_components/hamburger-icon/..
````

## Settings

You can change the settings:

 * width — *default: 32px*;
 * height — *default: 3px*;
 * gutter — *default: 5px*;
 * color — *default:  #000*;
 * border-radius — *default: 0*;
 * duration — *default: .3s*;
 * timing-function — *default: ease*;

## How to use

**HTML:**

````HTML
<button class="navigation-toggle" data-tools="collapse" data-target="#globalNavbar">
  <span class="menu-icon"></span>
</button>
```

**Less:**

Required mixin of settings `.hamburger-settings()`.

````Less
.hamburger-settings(24px, 3px, 5px, #777, @timing-function: linear);

.menu-icon {
  .hamburger-generator();
}

.navigation-toggle {
  &.active .menu-icon {
    .hamburger-animation();
  }
}
````

**SASS:**

````scss
.menu-icon {
  @include hamburger-generator(24px, 3px, 5px, #777, $timing-function: linear);
}

.navigation-toggle {
  &.active .menu-icon {
    @include hamburger-animation();
  }
}
````

**Stylus:**

````Stylus
.menu-icon
  hamburger-generator(24px, 3px, 5px, #777, $timing-function: linear)

.navigation-toggle
  &.active .menu-icon
    hamburger-animation()
````

## Changelog

See the [Releases section of our GitHub project](https://github.com/mrmlnc/hamburger-icon/releases) for changelogs for each release version.

## License

This software is released under the terms of the MIT license.