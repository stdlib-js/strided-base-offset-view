<!--

@license Apache-2.0

Copyright (c) 2021 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# offsetView

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return a typed array view having the same data type as a provided input typed array and starting at a specified index offset.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
offsetView = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/strided-base-offset-view@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var offsetView = require( 'path/to/vendor/umd/strided-base-offset-view/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/strided-base-offset-view@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.offsetView;
})();
</script>
```

#### offsetView( x, offset )

Returns a typed array view having the same data type as a provided input typed array and starting at a specified index offset.

```javascript
var Float64Array = require( '@stdlib/array-float64' );

var x = new Float64Array( 10 );

var view = offsetView( x, 0 );
// returns <Float64Array>

var bool = ( view.buffer === x.buffer );
// returns true

var len = view.length;
// returns 10
```

The `offset` argument specifies the starting index of the returned typed array view relative to the input array `x`.

```javascript
var Float64Array = require( '@stdlib/array-float64' );

var x = new Float64Array( [ 1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0 ] );

var view = offsetView( x, 2 );
// returns <Float64Array>

var len = view.length;
// returns 6

var v1 = view[ 0 ];
// returns 3.0

var v2 = view[ 1 ];
// returns 4.0
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/array-float64@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/strided-base-offset-view@umd/browser.js"></script>
<script type="text/javascript">
(function () {

// Define a typed array:
var x = new Float64Array( [ 1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0 ] );
// returns <Float64Array>

// Create a view of the array:
var view = offsetView( x, 0 );
// returns <Float64Array>

// Set view elements:
view[ 0 ] = 9.0;
view[ 1 ] = 10.0;

// Get the first two elements of the original array:
var v0 = x[ 0 ];
// returns 9.0

var v1 = x[ 1 ];
// returns 10.0

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/strided-base/min-view-buffer-index`][@stdlib/strided/base/min-view-buffer-index]</span><span class="delimiter">: </span><span class="description">return the minimum accessible index based on a set of provided strided array parameters.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/strided-base-offset-view.svg
[npm-url]: https://npmjs.org/package/@stdlib/strided-base-offset-view

[test-image]: https://github.com/stdlib-js/strided-base-offset-view/actions/workflows/test.yml/badge.svg?branch=v0.2.3
[test-url]: https://github.com/stdlib-js/strided-base-offset-view/actions/workflows/test.yml?query=branch:v0.2.3

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/strided-base-offset-view/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/strided-base-offset-view?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/strided-base-offset-view.svg
[dependencies-url]: https://david-dm.org/stdlib-js/strided-base-offset-view/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/strided-base-offset-view/tree/deno
[deno-readme]: https://github.com/stdlib-js/strided-base-offset-view/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/strided-base-offset-view/tree/umd
[umd-readme]: https://github.com/stdlib-js/strided-base-offset-view/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/strided-base-offset-view/tree/esm
[esm-readme]: https://github.com/stdlib-js/strided-base-offset-view/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/strided-base-offset-view/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/strided-base-offset-view/main/LICENSE

<!-- <related-links> -->

[@stdlib/strided/base/min-view-buffer-index]: https://github.com/stdlib-js/strided-base-min-view-buffer-index/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
