# wlq-postcss-bem
修改自 [kezzbracey/postcss-bem](https://github.com/kezzbracey/postcss-bem)，使其能够支持webpack4以上版本。并增加指令的简写模式

# WLQ PostCSS Bem

```css

/* or @u */
@utility utilityName {
    color: green;
}

@utility utilityName small {
    color: blue;
}

/* or @b */
@component ComponentName {
    color: cyan;

    /* or @m */
    @modifier modifierName {
        color: yellow;
    }
  
    /* or @e */
    @descendent descendentName {
        color: navy;
    }

    /* or @w */
    @when stateName {
        color: crimson;
    }
}

@component-namespace nmsp {
    @component ComponentName {
        color: red;
    }
}
```

```css
.u-utilityName {
    color: green;
}

.u-sm-utilityName {
    color: blue;
}

.ComponentName {
    color: cyan;
}

.ComponentName--modifierName {
    color: yellow;
}

.ComponentName-descendentName {
    color: navy;
}

.ComponentName.is-stateName {
    color: crimson;
}

.nmsp-ComponentName {
    color: red;
}
```

## Usage

```js
postcss([ require('postcss-bem')({
    defaultNamespace: undefined, // default namespace to use, none by default
    style: 'suit' // suit or bem, suit by default
}) ])
```

See [PostCSS] docs for examples for your environment.
[PostCSS]: https://github.com/postcss/postcss
