# yearn-web-themes

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

Theming system for Yearn Finance and associated projects.  
A theme is a set of colors (could expand). A theme object looks like this
```js
{
	name: 'light',
	colors: {
		background: '#F4F7FB',
		backgroundVariant: '#E0EAFF',
		surface: '#FFFFFF',
		surfaceVariant: '#F9FBFD',
		primary: '#0657F9',
		primaryVariant: '#004ADF',
		secondary: '#E0EAFF',
		titles: '#001746',
		titlesVariant: '#0657F9',
		texts: '#7F8DA9',
		disabled: '#CED5E3',
		icons: {
			primary: '#CED5E3',
			variant: '#475570'
		},
		button: {
			filled: {
				primary: '#0657F9',
				variant: '#004ADF',
				text: '#FFFFFF',
			},
			outlined: {
				primary: '#FFFFFF',
				variant: '#E0EAFF',
				text: '#0657F9',
			},
			disabled: {
				primary: '#F4F7FB',
				text: '#CED5E3',
			}
		}
	}
}
```

Support themes are `light`, `dark` and `blue`.

## Install
This package is handled by Github's system. In order to be able to install it, first add the following to your `.npmrc` or `.yarnrc` file:
```
# For .npmrc
@yearn:registry=https://npm.pkg.github.com
```

```
# For .yarnrc
registry=https://npm.pkg.github.com/yearn
```

Then you can install is as usual:
```bash
yarn add @yearn/yearn-web-assets
```

## Usage

```jsx
import React, { Component, useState } from 'react'
import themes from 'yearn-web-themes'

class Example extends Component {
  const [theme, set_theme] = React.useState(themes.light)
  render() {
    return (
      <div className={'my-box-className'} style={{background: theme.colors.background}}>
        <h1 style={{color: theme.colors.title}}>Hello World</h1>
      </div>
    )
  }
}
```
