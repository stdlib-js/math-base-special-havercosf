<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

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

# Havercosine

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the half-value [versed cosine][versed-cosine] of a single-precision floating-point number (in radians).

<section class="intro">

The half-value [versed cosine][versed-cosine] is defined as

<!-- <equation class="equation" label="eq:havercosine" align="center" raw="\operatorname{havercos}(\theta) = \frac{1 + \cos \theta}{2}" alt="Haversed cosine."> -->

```math
\mathop{\mathrm{havercos}}(\theta) = \frac{1 + \cos \theta}{2}
```

<!-- </equation> -->

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-havercosf
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var havercosf = require( '@stdlib/math-base-special-havercosf' );
```

#### havercosf( x )

Computes the half-value [versed cosine][versed-cosine] of a single-precision floating-point number (in radians).

```javascript
var v = havercosf( 0.0 );
// returns 1.0

v = havercosf( 3.141592653589793/2.0 );
// returns 0.5

v = havercosf( -3.141592653589793/6.0 );
// returns ~0.9330
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var uniform = require( '@stdlib/random-array-uniform' );
var logEachMap = require( '@stdlib/console-log-each-map' );
var TWO_PI = require( '@stdlib/constants-float32-two-pi' );
var havercosf = require( '@stdlib/math-base-special-havercosf' );

var opts = {
    'dtype': 'float32'
};
var x = uniform( 100, 0.0, TWO_PI, opts );

logEachMap( 'havercosf(%0.4f) = %0.4f', x, havercosf );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/math/base/special/havercosf.h"
```

#### stdlib_base_havercosf( x )

Computes the half-value [versed cosine][versed-cosine] of a single-precision floating-point number (in radians).

```c
float out = stdlib_base_havercosf( 0.0f );
// returns 1.0f

out = stdlib_base_havercosf( 3.141592653589793f / 2.0f );
// returns 0.5f
```

The function accepts the following arguments:

-   **x**: `[in] float` input value.

```c
float stdlib_base_havercosf( const float x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/special/havercosf.h"
#include <stdio.h>

int main( void ) {
    const float x[] = { 0.0f, 0.523f, 0.785f, 1.047f, 3.14f };

    float y;
    int i;
    for ( i = 0; i < 5; i++ ) {
        y = stdlib_base_havercosf( x[ i ] );
        printf( "havercosf(%f) = %f\n", x[ i ], y );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-havercosf.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-havercosf

[test-image]: https://github.com/stdlib-js/math-base-special-havercosf/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-havercosf/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-havercosf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-havercosf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-havercosf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-havercosf/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-havercosf/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-havercosf/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-havercosf/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-havercosf/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-havercosf/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-havercosf/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-havercosf/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-havercosf/main/LICENSE

[versed-cosine]: https://en.wikipedia.org/wiki/Versine

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
