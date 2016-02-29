# okaynav

> Progressively Collapsing Navigation Links

[![NPM Version][npm-img]][npm] [![Build Status][ci-img]][ci] [![Chat room][chat-img]][chat] 

[okaynav] is a responsive and mobile-friendly navigation plugin that automatically hides overflowing items and shows them in a off-canvas sidebar navigation when screen's size is too small to fit all menu items.

![okaynav demo](https://raw.githubusercontent.com/VPenkov/okayNav/master/demo.gif)

## Usage

```html
<header>
	<h1>Logo</h1>
	<nav id="navigation">
		<ul>
			<li><a href="/shop">Shop</a></li>
			<li><a href="/blog">Blog</a></li>
			...
		</ul>
	</nav>
</header>
```

```js
var okaynav = new OkayNav(target, options);
```

##### target
**Type**: `Selector` || `Element`

The element containing navigation items.

## Options

Optionally, you may override any of [okaynav]’s configuration.

##### measure
**Type**: `Selector` || `Element`  
**Default**: `target.parentNode`

The element whose width and children’s widths determine the overflow.

##### items
**Type**: `Selector` || `Array-like`  
**Default**: `target.querySelector("li")`

The items which may be overflowed.

##### toggle
**Type**: `Selector` || `Element`  
**Default**: `target.appendChild(document.createElement("ul")`

The element toggling the visibility of overflowed navigation.

##### overflow
**Type**: `Selector` || `Element`  
**Default**: `target.appendChild(document.createElement("ul"))`

The element containing overflowed items.

##### toggleContent
**Type**: `HTML` || `Element`  
**Default**: `⋮`

The contents of the toggle element.

##### priority
**Type**: `Attribute` || `Function`  
**Default**: `data-order`

The method used to prioritize navigation items from being overflowed.

## Events

[okaynav] dispatches many bubbling custom events you may find useful.

##### okaynav:initialized

Dispatched from the target when okaynav is activated.

##### okaynav:removeitem

Dispatched from an item when it is hidden from the navigation.

##### okaynav:additem

Dispatched from an item when it is added back to the navigation.

##### okaynav:showtoggle

Dispatched from the target when the toggle element becomes visible.

##### okaynav:hidetoggle

Dispatched from the target when the toggle element becomes hidden.

##### okaynav:showoverflow

Dispatched from the target when the overflow navigation becomes visible.

##### okaynav:hideoverflow

Dispatched from the target when the overflow navigation becomes hidden.

## Accessibility

ARIA attributes are automatically added to and toggled on elements to improve the accessibility of overflowed navigation.

- The toggle element is given an **aria-expanded** attribute which is true when overflowed navigation is visible and false when it is hidden.

- The toggle element is given an **aria-expanded** attribute which is true when overflowed navigation is visible and false when it is hidden.

aria-haspopup="true"

aria-label="submenu"

[chat]:     https://gitter.im/VPenkov/okayNav
[chat-img]: https://img.shields.io/gitter/room/nwjs/nw.js.svg
[ci]:       https://travis-ci.org/VPenkov/okaynav
[ci-img]:   https://img.shields.io/travis/VPenkov/okaynav.svg
[npm]:      https://www.npmjs.com/package/okaynav
[npm-img]:  https://img.shields.io/npm/v/okaynav.svg

[okaynav]: https://github.com/VPenkov/okayNav-vanillaJS
