<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Assert

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Assertion utilities.

<section class="installation">

## Installation

```bash
npm install @patrtorg/quos-quasi-ipsa
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
var assert = require( '@patrtorg/quos-quasi-ipsa' );
```

#### assert

Namespace providing utilities for data type testing and feature detection.

```javascript
var o = assert;
// returns {...}
```

To validate the built-in JavaScript data types, the namespace includes the following assertion utilities:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArray( value )`][@patrtorg/quos-quasi-ipsa/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="signature">[`isBoolean( value )`][@patrtorg/quos-quasi-ipsa/is-boolean]</span><span class="delimiter">: </span><span class="description">test if a value is a boolean.</span>
-   <span class="signature">[`isDateObject( value )`][@patrtorg/quos-quasi-ipsa/is-date-object]</span><span class="delimiter">: </span><span class="description">test if a value is a Date object.</span>
-   <span class="signature">[`isFunction( value )`][@patrtorg/quos-quasi-ipsa/is-function]</span><span class="delimiter">: </span><span class="description">test if a value is a function.</span>
-   <span class="signature">[`isnan( value )`][@patrtorg/quos-quasi-ipsa/is-nan]</span><span class="delimiter">: </span><span class="description">test if a value is NaN.</span>
-   <span class="signature">[`isNull( value )`][@patrtorg/quos-quasi-ipsa/is-null]</span><span class="delimiter">: </span><span class="description">test if a value is null.</span>
-   <span class="signature">[`isNumber( value )`][@patrtorg/quos-quasi-ipsa/is-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number.</span>
-   <span class="signature">[`isObject( value )`][@patrtorg/quos-quasi-ipsa/is-object]</span><span class="delimiter">: </span><span class="description">test if a value is an object.</span>
-   <span class="signature">[`isRegExp( value )`][@patrtorg/quos-quasi-ipsa/is-regexp]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression.</span>
-   <span class="signature">[`isString( value )`][@patrtorg/quos-quasi-ipsa/is-string]</span><span class="delimiter">: </span><span class="description">test if a value is a string.</span>
-   <span class="signature">[`isSymbol( value )`][@patrtorg/quos-quasi-ipsa/is-symbol]</span><span class="delimiter">: </span><span class="description">test if a value is a symbol.</span>
-   <span class="signature">[`isUndefined( value )`][@patrtorg/quos-quasi-ipsa/is-undefined]</span><span class="delimiter">: </span><span class="description">test if a value is undefined.</span>

</div>

<!-- </toc> -->

For primitive types having corresponding object wrappers, assertion utilities provide `isObject` and `isPrimitive` methods to test for either objects or primitives, respectively.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Boolean = require( '@stdlib/boolean/ctor' );
var isBoolean = require( '@patrtorg/quos-quasi-ipsa/is-boolean' );

var bool = isBoolean.isObject( new Boolean( false ) );
// returns true

bool = isBoolean.isObject( false );
// returns false

bool = isBoolean.isPrimitive( false );
// returns true
```

Many of the assertion utilities have corresponding packages that test whether array elements are of the given data type:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|nan|number|object|regexp|symbol|null|undefined)-array" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArrayArray( value )`][@patrtorg/quos-quasi-ipsa/is-array-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of arrays.</span>
-   <span class="signature">[`isBooleanArray( value )`][@patrtorg/quos-quasi-ipsa/is-boolean-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of booleans.</span>
-   <span class="signature">[`isDateObjectArray( value )`][@patrtorg/quos-quasi-ipsa/is-date-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only Date objects.</span>
-   <span class="signature">[`isFunctionArray( value )`][@patrtorg/quos-quasi-ipsa/is-function-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only functions.</span>
-   <span class="signature">[`isNaNArray( value )`][@patrtorg/quos-quasi-ipsa/is-nan-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only NaN values.</span>
-   <span class="signature">[`isNullArray( value )`][@patrtorg/quos-quasi-ipsa/is-null-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only null values.</span>
-   <span class="signature">[`isNumberArray( value )`][@patrtorg/quos-quasi-ipsa/is-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of numbers.</span>
-   <span class="signature">[`isObjectArray( value )`][@patrtorg/quos-quasi-ipsa/is-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only objects.</span>
-   <span class="signature">[`isStringArray( value )`][@patrtorg/quos-quasi-ipsa/is-string-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of strings.</span>
-   <span class="signature">[`isSymbolArray( value )`][@patrtorg/quos-quasi-ipsa/is-symbol-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only symbols.</span>

</div>

<!-- </toc> -->

Where applicable, similar to the assertion utilities for built-in data types, array assertion utilities provides methods for testing for an array of primitives or objects.

<!-- eslint-disable no-new-wrappers -->

```javascript
var isStringArray = require( '@patrtorg/quos-quasi-ipsa/is-string-array' );

var bool = isStringArray( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.primitives( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.objects( [ 'hello', 'world' ] );
// returns false

bool = isStringArray.objects( [ new String( 'hello' ), new String( 'world' ) ] );
// returns true
```

The namespace also contains utilities to test for numbers within a certain range or for numbers satisfying a particular "type":

<!-- <toc pattern="is-*+(number|integer)*" ignore="is-number-array" ignore="is-number" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCubeNumber( value )`][@patrtorg/quos-quasi-ipsa/is-cube-number]</span><span class="delimiter">: </span><span class="description">test if a value is a cube number.</span>
-   <span class="signature">[`isIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only integers.</span>
-   <span class="signature">[`isInteger( value )`][@patrtorg/quos-quasi-ipsa/is-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having an integer value.</span>
-   <span class="signature">[`isNegativeIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-negative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative integers.</span>
-   <span class="signature">[`isNegativeInteger( value )`][@patrtorg/quos-quasi-ipsa/is-negative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative integer value.</span>
-   <span class="signature">[`isNegativeNumberArray( value )`][@patrtorg/quos-quasi-ipsa/is-negative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative numbers.</span>
-   <span class="signature">[`isNegativeNumber( value )`][@patrtorg/quos-quasi-ipsa/is-negative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative value.</span>
-   <span class="signature">[`isNonNegativeIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-nonnegative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative integers.</span>
-   <span class="signature">[`isNonNegativeInteger( value )`][@patrtorg/quos-quasi-ipsa/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative integer value.</span>
-   <span class="signature">[`isNonNegativeNumberArray( value )`][@patrtorg/quos-quasi-ipsa/is-nonnegative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative numbers.</span>
-   <span class="signature">[`isNonNegativeNumber( value )`][@patrtorg/quos-quasi-ipsa/is-nonnegative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative value.</span>
-   <span class="signature">[`isNonPositiveIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-nonpositive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive integers.</span>
-   <span class="signature">[`isNonPositiveInteger( value )`][@patrtorg/quos-quasi-ipsa/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive integer value.</span>
-   <span class="signature">[`isNonPositiveNumberArray( value )`][@patrtorg/quos-quasi-ipsa/is-nonpositive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive numbers.</span>
-   <span class="signature">[`isNonPositiveNumber( value )`][@patrtorg/quos-quasi-ipsa/is-nonpositive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive value.</span>
-   <span class="signature">[`isPositiveIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-positive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive integers.</span>
-   <span class="signature">[`isPositiveInteger( value )`][@patrtorg/quos-quasi-ipsa/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive integer value.</span>
-   <span class="signature">[`isPositiveNumberArray( value )`][@patrtorg/quos-quasi-ipsa/is-positive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive numbers.</span>
-   <span class="signature">[`isPositiveNumber( value )`][@patrtorg/quos-quasi-ipsa/is-positive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive value.</span>
-   <span class="signature">[`isSafeIntegerArray( value )`][@patrtorg/quos-quasi-ipsa/is-safe-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only safe integers.</span>
-   <span class="signature">[`isSafeInteger( value )`][@patrtorg/quos-quasi-ipsa/is-safe-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a safe integer value.</span>
-   <span class="signature">[`isSquareNumber( value )`][@patrtorg/quos-quasi-ipsa/is-square-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square number.</span>
-   <span class="signature">[`isSquareTriangularNumber( value )`][@patrtorg/quos-quasi-ipsa/is-square-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square triangular number.</span>
-   <span class="signature">[`isTriangularNumber( value )`][@patrtorg/quos-quasi-ipsa/is-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a triangular number.</span>

</div>

<!-- </toc> -->

The namespace provides utilities for validating typed arrays:

<!-- <toc pattern="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array"> -->

<div class="namespace-toc">

-   <span class="signature">[`isFloat32Array( value )`][@patrtorg/quos-quasi-ipsa/is-float32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float32Array.</span>
-   <span class="signature">[`isFloat64Array( value )`][@patrtorg/quos-quasi-ipsa/is-float64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float64Array.</span>
-   <span class="signature">[`isInt16Array( value )`][@patrtorg/quos-quasi-ipsa/is-int16array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int16Array.</span>
-   <span class="signature">[`isInt32Array( value )`][@patrtorg/quos-quasi-ipsa/is-int32array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int32Array.</span>
-   <span class="signature">[`isInt8Array( value )`][@patrtorg/quos-quasi-ipsa/is-int8array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int8Array.</span>
-   <span class="signature">[`isUint16Array( value )`][@patrtorg/quos-quasi-ipsa/is-uint16array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint16Array.</span>
-   <span class="signature">[`isUint32Array( value )`][@patrtorg/quos-quasi-ipsa/is-uint32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint32Array.</span>
-   <span class="signature">[`isUint8Array( value )`][@patrtorg/quos-quasi-ipsa/is-uint8array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8Array.</span>
-   <span class="signature">[`isUint8ClampedArray( value )`][@patrtorg/quos-quasi-ipsa/is-uint8clampedarray]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8ClampedArray.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating `ndarray`s (n-dimensional arrays).

<!-- <toc keywords="+ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCentrosymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a centrosymmetric matrix.</span>
-   <span class="signature">[`isComplex128MatrixLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex128matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128ndarrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex128ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128VectorLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex128vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64MatrixLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64ndarrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64VectorLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isFloat32MatrixLike( value )`][@patrtorg/quos-quasi-ipsa/is-float32matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32ndarrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-float32ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32VectorLike( value )`][@patrtorg/quos-quasi-ipsa/is-float32vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64MatrixLike( value )`][@patrtorg/quos-quasi-ipsa/is-float64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64ndarrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-float64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64VectorLike( value )`][@patrtorg/quos-quasi-ipsa/is-float64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isMatrixLike( value )`][@patrtorg/quos-quasi-ipsa/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is 2-dimensional ndarray-like object.</span>
-   <span class="signature">[`isndarrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is ndarray-like.</span>
-   <span class="signature">[`isNonSymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-nonsymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a non-symmetric matrix.</span>
-   <span class="signature">[`isPersymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a persymmetric matrix.</span>
-   <span class="signature">[`isSkewCentrosymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-skew-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-centrosymmetric matrix.</span>
-   <span class="signature">[`isSkewPersymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-skew-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-persymmetric matrix.</span>
-   <span class="signature">[`isSkewSymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-skew-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-symmetric matrix.</span>
-   <span class="signature">[`isSquareMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-square-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object having equal dimensions.</span>
-   <span class="signature">[`isSymmetricMatrix( value )`][@patrtorg/quos-quasi-ipsa/is-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a symmetric matrix.</span>
-   <span class="signature">[`isVectorLike( value )`][@patrtorg/quos-quasi-ipsa/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating complex numbers and arrays of complex numbers:

<!-- <toc pattern="is-complex*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isComplexLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex-like]</span><span class="delimiter">: </span><span class="description">test if a value is a complex number-like object.</span>
-   <span class="signature">[`isComplexTypedArrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-complex-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is complex-typed-array-like.</span>
-   <span class="signature">[`isComplexTypedArray( value )`][@patrtorg/quos-quasi-ipsa/is-complex-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a complex typed array.</span>
-   <span class="signature">[`isComplex( value )`][@patrtorg/quos-quasi-ipsa/is-complex]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit or 128-bit complex number.</span>
-   <span class="signature">[`isComplex128( value )`][@patrtorg/quos-quasi-ipsa/is-complex128]</span><span class="delimiter">: </span><span class="description">test if a value is a 128-bit complex number.</span>
-   <span class="signature">[`isComplex128Array( value )`][@patrtorg/quos-quasi-ipsa/is-complex128array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex128Array.</span>
-   <span class="signature">[`isComplex64( value )`][@patrtorg/quos-quasi-ipsa/is-complex64]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit complex number.</span>
-   <span class="signature">[`isComplex64Array( value )`][@patrtorg/quos-quasi-ipsa/is-complex64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex64Array.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating other special arrays or buffers:

<!-- <toc pattern="is-*array*" ignore="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array" ignore="is-*+(number|integer)*" ignore="is-+(array|boolean|date-object|function|string|nan|number|object|primitive|regexp|symbol|null|undefined)-array" ignore="is-array" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isAccessorArray( value )`][@patrtorg/quos-quasi-ipsa/is-accessor-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object supporting the accessor (get/set) protocol.</span>
-   <span class="signature">[`isArrayLength( value )`][@patrtorg/quos-quasi-ipsa/is-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid array length.</span>
-   <span class="signature">[`isArrayLikeObject( value )`][@patrtorg/quos-quasi-ipsa/is-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object.</span>
-   <span class="signature">[`isArrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="signature">[`isArrayBufferView( value )`][@patrtorg/quos-quasi-ipsa/is-arraybuffer-view]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer view.</span>
-   <span class="signature">[`isArrayBuffer( value )`][@patrtorg/quos-quasi-ipsa/is-arraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer.</span>
-   <span class="signature">[`isBetweenArray( value, a, b[, left, right] )`][@patrtorg/quos-quasi-ipsa/is-between-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object where every element is between two values.</span>
-   <span class="signature">[`isBigInt64Array( value )`][@patrtorg/quos-quasi-ipsa/is-bigint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt64Array.</span>
-   <span class="signature">[`isBigUint64Array( value )`][@patrtorg/quos-quasi-ipsa/is-biguint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigUint64Array.</span>
-   <span class="signature">[`isCircularArray( value )`][@patrtorg/quos-quasi-ipsa/is-circular-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array containing a circular reference.</span>
-   <span class="signature">[`isEmptyArrayLikeObject( value )`][@patrtorg/quos-quasi-ipsa/is-empty-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array-like object.</span>
-   <span class="signature">[`isEmptyArray( value )`][@patrtorg/quos-quasi-ipsa/is-empty-array]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array.</span>
-   <span class="signature">[`isFalsyArray( value )`][@patrtorg/quos-quasi-ipsa/is-falsy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only falsy values.</span>
-   <span class="signature">[`isFiniteArray( value )`][@patrtorg/quos-quasi-ipsa/is-finite-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only finite numbers.</span>
-   <span class="signature">[`isNumericArray( value )`][@patrtorg/quos-quasi-ipsa/is-numeric-array]</span><span class="delimiter">: </span><span class="description">test if a value is a numeric array.</span>
-   <span class="signature">[`isPlainObjectArray( value )`][@patrtorg/quos-quasi-ipsa/is-plain-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only plain objects.</span>
-   <span class="signature">[`isProbabilityArray( value )`][@patrtorg/quos-quasi-ipsa/is-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only probabilities.</span>
-   <span class="signature">[`isSameArray( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both generic arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex128Array( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-complex128array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex128Arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex64Array( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-complex64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex64Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat32Array( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-float32array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float32Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat64Array( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-float64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float64Arrays and have the same values.</span>
-   <span class="signature">[`isSharedArrayBuffer( value )`][@patrtorg/quos-quasi-ipsa/is-sharedarraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is a SharedArrayBuffer.</span>
-   <span class="signature">[`isTruthyArray( value )`][@patrtorg/quos-quasi-ipsa/is-truthy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only truthy values.</span>
-   <span class="signature">[`isTypedArrayLength( value )`][@patrtorg/quos-quasi-ipsa/is-typed-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid typed array length.</span>
-   <span class="signature">[`isTypedArrayLike( value )`][@patrtorg/quos-quasi-ipsa/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="signature">[`isTypedArray( value )`][@patrtorg/quos-quasi-ipsa/is-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a typed array.</span>
-   <span class="signature">[`isUnityProbabilityArray( value )`][@patrtorg/quos-quasi-ipsa/is-unity-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of probabilities that sum to one.</span>

</div>

<!-- </toc> -->

To test for error objects, the namespace includes the following utilities:

<!-- <toc pattern="is-*error*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isError( value )`][@patrtorg/quos-quasi-ipsa/is-error]</span><span class="delimiter">: </span><span class="description">test if a value is an Error object.</span>
-   <span class="signature">[`isEvalError( value )`][@patrtorg/quos-quasi-ipsa/is-eval-error]</span><span class="delimiter">: </span><span class="description">test if a value is an EvalError object.</span>
-   <span class="signature">[`isRangeError( value )`][@patrtorg/quos-quasi-ipsa/is-range-error]</span><span class="delimiter">: </span><span class="description">test if a value is a RangeError object.</span>
-   <span class="signature">[`isReferenceError( value )`][@patrtorg/quos-quasi-ipsa/is-reference-error]</span><span class="delimiter">: </span><span class="description">test if a value is a ReferenceError object.</span>
-   <span class="signature">[`isSyntaxError( value )`][@patrtorg/quos-quasi-ipsa/is-syntax-error]</span><span class="delimiter">: </span><span class="description">test if a value is a SyntaxError object.</span>
-   <span class="signature">[`isTypeError( value )`][@patrtorg/quos-quasi-ipsa/is-type-error]</span><span class="delimiter">: </span><span class="description">test if a value is a TypeError object.</span>
-   <span class="signature">[`isURIError( value )`][@patrtorg/quos-quasi-ipsa/is-uri-error]</span><span class="delimiter">: </span><span class="description">test if a value is a URIError object.</span>

</div>

<!-- </toc> -->

The namespace exposes the following constants concerning the current running process:

<!-- <toc pattern="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|big-endian|node|web-worker|windows|docker|mobile|touch-device)" > -->

<div class="namespace-toc">

-   <span class="signature">[`IS_BIG_ENDIAN`][@patrtorg/quos-quasi-ipsa/is-big-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is big endian.</span>
-   <span class="signature">[`IS_BROWSER`][@patrtorg/quos-quasi-ipsa/is-browser]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web browser.</span>
-   <span class="signature">[`IS_DARWIN`][@patrtorg/quos-quasi-ipsa/is-darwin]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Darwin.</span>
-   <span class="signature">[`IS_DOCKER`][@patrtorg/quos-quasi-ipsa/is-docker]</span><span class="delimiter">: </span><span class="description">check if the process is running in a Docker container.</span>
-   <span class="signature">[`IS_ELECTRON_MAIN`][@patrtorg/quos-quasi-ipsa/is-electron-main]</span><span class="delimiter">: </span><span class="description">check if the runtime is the main Electron process.</span>
-   <span class="signature">[`IS_ELECTRON_RENDERER`][@patrtorg/quos-quasi-ipsa/is-electron-renderer]</span><span class="delimiter">: </span><span class="description">check if the runtime is the Electron renderer process.</span>
-   <span class="signature">[`IS_ELECTRON`][@patrtorg/quos-quasi-ipsa/is-electron]</span><span class="delimiter">: </span><span class="description">check if the runtime is Electron.</span>
-   <span class="signature">[`IS_LITTLE_ENDIAN`][@patrtorg/quos-quasi-ipsa/is-little-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is little endian.</span>
-   <span class="signature">[`IS_MOBILE`][@patrtorg/quos-quasi-ipsa/is-mobile]</span><span class="delimiter">: </span><span class="description">check if the current environment is a mobile device.</span>
-   <span class="signature">[`IS_NODE`][@patrtorg/quos-quasi-ipsa/is-node]</span><span class="delimiter">: </span><span class="description">check if the runtime is Node.js.</span>
-   <span class="signature">[`IS_TOUCH_DEVICE`][@patrtorg/quos-quasi-ipsa/is-touch-device]</span><span class="delimiter">: </span><span class="description">check if the current environment is a touch device.</span>
-   <span class="signature">[`IS_WEB_WORKER`][@patrtorg/quos-quasi-ipsa/is-web-worker]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web worker.</span>
-   <span class="signature">[`IS_WINDOWS`][@patrtorg/quos-quasi-ipsa/is-windows]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Windows.</span>

</div>

<!-- </toc> -->

To test whether a runtime environment supports certain features, the namespace includes the following utilities:

<!-- <toc pattern="has-*-support" > -->

<div class="namespace-toc">

-   <span class="signature">[`hasArrayBufferSupport()`][@patrtorg/quos-quasi-ipsa/has-arraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `ArrayBuffer` support.</span>
-   <span class="signature">[`hasArrowFunctionSupport()`][@patrtorg/quos-quasi-ipsa/has-arrow-function-support]</span><span class="delimiter">: </span><span class="description">detect native `arrow function` support.</span>
-   <span class="signature">[`hasAsyncAwaitSupport()`][@patrtorg/quos-quasi-ipsa/has-async-await-support]</span><span class="delimiter">: </span><span class="description">detect native `async`/`await` support.</span>
-   <span class="signature">[`hasAsyncIteratorSymbolSupport()`][@patrtorg/quos-quasi-ipsa/has-async-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.asyncIterator` support.</span>
-   <span class="signature">[`hasBigIntSupport()`][@patrtorg/quos-quasi-ipsa/has-bigint-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt` support.</span>
-   <span class="signature">[`hasBigInt64ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-bigint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt64Array` support.</span>
-   <span class="signature">[`hasBigUint64ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-biguint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigUint64Array` support.</span>
-   <span class="signature">[`hasClassSupport()`][@patrtorg/quos-quasi-ipsa/has-class-support]</span><span class="delimiter">: </span><span class="description">detect native `class` support.</span>
-   <span class="signature">[`hasDataViewSupport()`][@patrtorg/quos-quasi-ipsa/has-dataview-support]</span><span class="delimiter">: </span><span class="description">detect native `DataView` support.</span>
-   <span class="signature">[`hasDefinePropertiesSupport()`][@patrtorg/quos-quasi-ipsa/has-define-properties-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperties` support.</span>
-   <span class="signature">[`hasDefinePropertySupport()`][@patrtorg/quos-quasi-ipsa/has-define-property-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperty` support.</span>
-   <span class="signature">[`hasFloat32ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-float32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float32Array` support.</span>
-   <span class="signature">[`hasFloat64ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-float64array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float64Array` support.</span>
-   <span class="signature">[`hasFunctionNameSupport()`][@patrtorg/quos-quasi-ipsa/has-function-name-support]</span><span class="delimiter">: </span><span class="description">detect native function `name` support.</span>
-   <span class="signature">[`hasGeneratorSupport()`][@patrtorg/quos-quasi-ipsa/has-generator-support]</span><span class="delimiter">: </span><span class="description">detect native `generator function` support.</span>
-   <span class="signature">[`hasGlobalThisSupport()`][@patrtorg/quos-quasi-ipsa/has-globalthis-support]</span><span class="delimiter">: </span><span class="description">detect `globalThis` support.</span>
-   <span class="signature">[`hasInt16ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-int16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int16Array` support.</span>
-   <span class="signature">[`hasInt32ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-int32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int32Array` support.</span>
-   <span class="signature">[`hasInt8ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-int8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int8Array` support.</span>
-   <span class="signature">[`hasIteratorSymbolSupport()`][@patrtorg/quos-quasi-ipsa/has-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.iterator` support.</span>
-   <span class="signature">[`hasMapSupport()`][@patrtorg/quos-quasi-ipsa/has-map-support]</span><span class="delimiter">: </span><span class="description">detect native `Map` support.</span>
-   <span class="signature">[`hasNodeBufferSupport()`][@patrtorg/quos-quasi-ipsa/has-node-buffer-support]</span><span class="delimiter">: </span><span class="description">detect native `Buffer` support.</span>
-   <span class="signature">[`hasProxySupport()`][@patrtorg/quos-quasi-ipsa/has-proxy-support]</span><span class="delimiter">: </span><span class="description">detect native `Proxy` support.</span>
-   <span class="signature">[`hasSetSupport()`][@patrtorg/quos-quasi-ipsa/has-set-support]</span><span class="delimiter">: </span><span class="description">detect native `Set` support.</span>
-   <span class="signature">[`hasSharedArrayBufferSupport()`][@patrtorg/quos-quasi-ipsa/has-sharedarraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `SharedArrayBuffer` support.</span>
-   <span class="signature">[`hasSymbolSupport()`][@patrtorg/quos-quasi-ipsa/has-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol` support.</span>
-   <span class="signature">[`hasToStringTagSupport()`][@patrtorg/quos-quasi-ipsa/has-tostringtag-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.toStringTag` support.</span>
-   <span class="signature">[`hasUint16ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-uint16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint16Array` support.</span>
-   <span class="signature">[`hasUint32ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-uint32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint32Array` support.</span>
-   <span class="signature">[`hasUint8ArraySupport()`][@patrtorg/quos-quasi-ipsa/has-uint8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8Array` support.</span>
-   <span class="signature">[`hasUint8ClampedArraySupport()`][@patrtorg/quos-quasi-ipsa/has-uint8clampedarray-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8ClampedArray` support.</span>
-   <span class="signature">[`hasWebAssemblySupport()`][@patrtorg/quos-quasi-ipsa/has-wasm-support]</span><span class="delimiter">: </span><span class="description">detect native WebAssembly support.</span>
-   <span class="signature">[`hasWeakMapSupport()`][@patrtorg/quos-quasi-ipsa/has-weakmap-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakMap` support.</span>
-   <span class="signature">[`hasWeakSetSupport()`][@patrtorg/quos-quasi-ipsa/has-weakset-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakSet` support.</span>

</div>

<!-- </toc> -->

The remaining namespace utilities are as follows:

<!-- <toc ignore="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" ignore="is-*+(number|integer)*" ignore="is-*array*" ignore="is-*error*" ignore="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|node|web-worker|windows)" ignore="has-*-support" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`contains( val, searchValue[, position] )`][@patrtorg/quos-quasi-ipsa/contains]</span><span class="delimiter">: </span><span class="description">test if an array-like value contains a search value.</span>
-   <span class="signature">[`deepEqual( a, b )`][@patrtorg/quos-quasi-ipsa/deep-equal]</span><span class="delimiter">: </span><span class="description">test for deep equality between two values.</span>
-   <span class="signature">[`deepHasOwnProp( value, path[, options] )`][@patrtorg/quos-quasi-ipsa/deep-has-own-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path.</span>
-   <span class="signature">[`deepHasProp( value, path[, options] )`][@patrtorg/quos-quasi-ipsa/deep-has-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path, either own or inherited.</span>
-   <span class="signature">[`hasOwnProp( value, property )`][@patrtorg/quos-quasi-ipsa/has-own-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property.</span>
-   <span class="signature">[`hasProp( value, property )`][@patrtorg/quos-quasi-ipsa/has-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property, either own or inherited.</span>
-   <span class="signature">[`hasUTF16SurrogatePairAt( string, position )`][@patrtorg/quos-quasi-ipsa/has-utf16-surrogate-pair-at]</span><span class="delimiter">: </span><span class="description">test if a position in a string marks the start of a UTF-16 surrogate pair.</span>
-   <span class="signature">[`instanceOf( value, constructor )`][@patrtorg/quos-quasi-ipsa/instance-of]</span><span class="delimiter">: </span><span class="description">test whether a value has in its prototype chain a specified constructor as a prototype property.</span>
-   <span class="signature">[`isAbsoluteHttpURI( value )`][@patrtorg/quos-quasi-ipsa/is-absolute-http-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute HTTP(S) URI.</span>
-   <span class="signature">[`isAbsolutePath( value )`][@patrtorg/quos-quasi-ipsa/is-absolute-path]</span><span class="delimiter">: </span><span class="description">test if a value is an absolute path.</span>
-   <span class="signature">[`isAbsoluteURI( value )`][@patrtorg/quos-quasi-ipsa/is-absolute-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute URI.</span>
-   <span class="signature">[`isAccessorPropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-accessor-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has an accessor descriptor.</span>
-   <span class="signature">[`isAccessorProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-accessor-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has an accessor descriptor.</span>
-   <span class="signature">[`isAlphagram( value )`][@patrtorg/quos-quasi-ipsa/is-alphagram]</span><span class="delimiter">: </span><span class="description">test if a value is an alphagram.</span>
-   <span class="signature">[`isAlphaNumeric( value )`][@patrtorg/quos-quasi-ipsa/is-alphanumeric]</span><span class="delimiter">: </span><span class="description">test whether a string contains only alphanumeric characters.</span>
-   <span class="signature">[`isAnagram( str, value )`][@patrtorg/quos-quasi-ipsa/is-anagram]</span><span class="delimiter">: </span><span class="description">test if a value is an anagram.</span>
-   <span class="signature">[`isArguments( value )`][@patrtorg/quos-quasi-ipsa/is-arguments]</span><span class="delimiter">: </span><span class="description">test if a value is an arguments object.</span>
-   <span class="signature">[`isArrowFunction( value )`][@patrtorg/quos-quasi-ipsa/is-arrow-function]</span><span class="delimiter">: </span><span class="description">test if a value is an `arrow function`.</span>
-   <span class="signature">[`isASCII( value )`][@patrtorg/quos-quasi-ipsa/is-ascii]</span><span class="delimiter">: </span><span class="description">test whether a character belongs to the ASCII character set and whether this is true for all characters in a provided string.</span>
-   <span class="signature">[`isBetween( value, a, b[, left, right] )`][@patrtorg/quos-quasi-ipsa/is-between]</span><span class="delimiter">: </span><span class="description">test if a value is between two values.</span>
-   <span class="signature">[`isBigInt( value )`][@patrtorg/quos-quasi-ipsa/is-bigint]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt.</span>
-   <span class="signature">[`isBinaryString( value )`][@patrtorg/quos-quasi-ipsa/is-binary-string]</span><span class="delimiter">: </span><span class="description">test if a value is a binary string.</span>
-   <span class="signature">[`isBlankString( value )`][@patrtorg/quos-quasi-ipsa/is-blank-string]</span><span class="delimiter">: </span><span class="description">test if a value is a blank string.</span>
-   <span class="signature">[`isBoxedPrimitive( value )`][@patrtorg/quos-quasi-ipsa/is-boxed-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript boxed primitive.</span>
-   <span class="signature">[`isBuffer( value )`][@patrtorg/quos-quasi-ipsa/is-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a Buffer object.</span>
-   <span class="signature">[`isCamelcase( value )`][@patrtorg/quos-quasi-ipsa/is-camelcase]</span><span class="delimiter">: </span><span class="description">test if a value is a camelcase string.</span>
-   <span class="signature">[`isCapitalized( value )`][@patrtorg/quos-quasi-ipsa/is-capitalized]</span><span class="delimiter">: </span><span class="description">test if a value is a string having an uppercase first character.</span>
-   <span class="signature">[`isCircular( value )`][@patrtorg/quos-quasi-ipsa/is-circular]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object containing a circular reference.</span>
-   <span class="signature">[`isCircular( value )`][@patrtorg/quos-quasi-ipsa/is-circular]</span><span class="delimiter">: </span><span class="description">test if an object-like value contains a circular reference.</span>
-   <span class="signature">[`isClass( value )`][@patrtorg/quos-quasi-ipsa/is-class]</span><span class="delimiter">: </span><span class="description">test if a value is a class.</span>
-   <span class="signature">[`isCollection( value )`][@patrtorg/quos-quasi-ipsa/is-collection]</span><span class="delimiter">: </span><span class="description">test if a value is a collection.</span>
-   <span class="signature">[`isComposite( value )`][@patrtorg/quos-quasi-ipsa/is-composite]</span><span class="delimiter">: </span><span class="description">test if a value is a composite number.</span>
-   <span class="signature">[`isConfigurablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-configurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is configurable.</span>
-   <span class="signature">[`isConfigurableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-configurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is configurable.</span>
-   <span class="signature">[`isConstantcase( value )`][@patrtorg/quos-quasi-ipsa/is-constantcase]</span><span class="delimiter">: </span><span class="description">test if a value is a constantcase string.</span>
-   <span class="signature">[`isCurrentYear( value )`][@patrtorg/quos-quasi-ipsa/is-current-year]</span><span class="delimiter">: </span><span class="description">test if a value is the current year.</span>
-   <span class="signature">[`isDataPropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-data-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has a data descriptor.</span>
-   <span class="signature">[`isDataProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-data-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has a data descriptor.</span>
-   <span class="signature">[`isDataView( value )`][@patrtorg/quos-quasi-ipsa/is-dataview]</span><span class="delimiter">: </span><span class="description">test if a value is a DataView.</span>
-   <span class="signature">[`isDigitString( value )`][@patrtorg/quos-quasi-ipsa/is-digit-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only numeric digits.</span>
-   <span class="signature">[`isDomainName( value )`][@patrtorg/quos-quasi-ipsa/is-domain-name]</span><span class="delimiter">: </span><span class="description">test if a value is a domain name.</span>
-   <span class="signature">[`isDurationString( value )`][@patrtorg/quos-quasi-ipsa/is-duration-string]</span><span class="delimiter">: </span><span class="description">test if a value is a duration string.</span>
-   <span class="signature">[`isEmailAddress( value )`][@patrtorg/quos-quasi-ipsa/is-email-address]</span><span class="delimiter">: </span><span class="description">test if a value is an email address.</span>
-   <span class="signature">[`isEmptyCollection( value )`][@patrtorg/quos-quasi-ipsa/is-empty-collection]</span><span class="delimiter">: </span><span class="description">test if a value is an empty collection.</span>
-   <span class="signature">[`isEmptyObject( value )`][@patrtorg/quos-quasi-ipsa/is-empty-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty object.</span>
-   <span class="signature">[`isEmptyString( value )`][@patrtorg/quos-quasi-ipsa/is-empty-string]</span><span class="delimiter">: </span><span class="description">test if a value is an empty string.</span>
-   <span class="signature">[`isEnumerablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-enumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is enumerable.</span>
-   <span class="signature">[`isEnumerableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-enumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is enumerable.</span>
-   <span class="signature">[`isEven( value )`][@patrtorg/quos-quasi-ipsa/is-even]</span><span class="delimiter">: </span><span class="description">test if a value is an even number.</span>
-   <span class="signature">[`isFalsy( value )`][@patrtorg/quos-quasi-ipsa/is-falsy]</span><span class="delimiter">: </span><span class="description">test if a value is falsy.</span>
-   <span class="signature">[`isFinite( value )`][@patrtorg/quos-quasi-ipsa/is-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a finite number.</span>
-   <span class="signature">[`isGeneratorObjectLike( value )`][@patrtorg/quos-quasi-ipsa/is-generator-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is `generator` object-like.</span>
-   <span class="signature">[`isGeneratorObject( value )`][@patrtorg/quos-quasi-ipsa/is-generator-object]</span><span class="delimiter">: </span><span class="description">test if a value is a `generator` object.</span>
-   <span class="signature">[`isgzipBuffer( value )`][@patrtorg/quos-quasi-ipsa/is-gzip-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a gzip buffer.</span>
-   <span class="signature">[`isHexString( value )`][@patrtorg/quos-quasi-ipsa/is-hex-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only hexadecimal digits.</span>
-   <span class="signature">[`isInfinite( value )`][@patrtorg/quos-quasi-ipsa/is-infinite]</span><span class="delimiter">: </span><span class="description">test if a value is an infinite number.</span>
-   <span class="signature">[`isInheritedProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-inherited-property]</span><span class="delimiter">: </span><span class="description">test if an object has an inherited property.</span>
-   <span class="signature">[`isIterableLike( value )`][@patrtorg/quos-quasi-ipsa/is-iterable-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterable`-like.</span>
-   <span class="signature">[`isIteratorLike( value )`][@patrtorg/quos-quasi-ipsa/is-iterator-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterator`-like.</span>
-   <span class="signature">[`isJSON( value )`][@patrtorg/quos-quasi-ipsa/is-json]</span><span class="delimiter">: </span><span class="description">test if a value is a parseable JSON string.</span>
-   <span class="signature">[`isKebabcase( value )`][@patrtorg/quos-quasi-ipsa/is-kebabcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in kebab case.</span>
-   <span class="signature">[`isLeapYear( [value] )`][@patrtorg/quos-quasi-ipsa/is-leap-year]</span><span class="delimiter">: </span><span class="description">test if a value corresponds to a leap year in the Gregorian calendar.</span>
-   <span class="signature">[`isLocalhost( value )`][@patrtorg/quos-quasi-ipsa/is-localhost]</span><span class="delimiter">: </span><span class="description">test whether a value is a localhost hostname.</span>
-   <span class="signature">[`isLowercase( value )`][@patrtorg/quos-quasi-ipsa/is-lowercase]</span><span class="delimiter">: </span><span class="description">test if a value is a lowercase string.</span>
-   <span class="signature">[`isMethodIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-method-in]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name, either own or inherited.</span>
-   <span class="signature">[`isMethod( value, property )`][@patrtorg/quos-quasi-ipsa/is-method]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name.</span>
-   <span class="signature">[`isMultiSlice( value )`][@patrtorg/quos-quasi-ipsa/is-multi-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `MultiSlice`.</span>
-   <span class="signature">[`isNamedTypedTupleLike( value )`][@patrtorg/quos-quasi-ipsa/is-named-typed-tuple-like]</span><span class="delimiter">: </span><span class="description">test if a value is named typed tuple-like.</span>
-   <span class="signature">[`isNativeFunction( value )`][@patrtorg/quos-quasi-ipsa/is-native-function]</span><span class="delimiter">: </span><span class="description">test if a value is a native function.</span>
-   <span class="signature">[`isNegativeZero( value )`][@patrtorg/quos-quasi-ipsa/is-negative-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to negative zero.</span>
-   <span class="signature">[`isNodeBuiltin( value )`][@patrtorg/quos-quasi-ipsa/is-node-builtin]</span><span class="delimiter">: </span><span class="description">test whether a string matches a Node.js built-in module name.</span>
-   <span class="signature">[`isNodeDuplexStreamLike( value )`][@patrtorg/quos-quasi-ipsa/is-node-duplex-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node duplex stream-like.</span>
-   <span class="signature">[`isNodeReadableStreamLike( value )`][@patrtorg/quos-quasi-ipsa/is-node-readable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node readable stream-like.</span>
-   <span class="signature">[`isNodeREPL()`][@patrtorg/quos-quasi-ipsa/is-node-repl]</span><span class="delimiter">: </span><span class="description">check if running in a Node.js REPL environment.</span>
-   <span class="signature">[`isNodeStreamLike( value )`][@patrtorg/quos-quasi-ipsa/is-node-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node stream-like.</span>
-   <span class="signature">[`isNodeTransformStreamLike( value )`][@patrtorg/quos-quasi-ipsa/is-node-transform-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node transform stream-like.</span>
-   <span class="signature">[`isNodeWritableStreamLike( value )`][@patrtorg/quos-quasi-ipsa/is-node-writable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node writable stream-like.</span>
-   <span class="signature">[`isNonConfigurablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-nonconfigurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-configurable.</span>
-   <span class="signature">[`isNonConfigurableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-nonconfigurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-configurable.</span>
-   <span class="signature">[`isNonEnumerablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-nonenumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-enumerable.</span>
-   <span class="signature">[`isNonEnumerableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-nonenumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-enumerable.</span>
-   <span class="signature">[`isNonNegativeFinite( value )`][@patrtorg/quos-quasi-ipsa/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative finite value.</span>
-   <span class="signature">[`isObjectLike( value )`][@patrtorg/quos-quasi-ipsa/is-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is object-like.</span>
-   <span class="signature">[`isOdd( value )`][@patrtorg/quos-quasi-ipsa/is-odd]</span><span class="delimiter">: </span><span class="description">test if a value is an odd number.</span>
-   <span class="signature">[`isPascalcase( value )`][@patrtorg/quos-quasi-ipsa/is-pascalcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in Pascal case.</span>
-   <span class="signature">[`isPlainObject( value )`][@patrtorg/quos-quasi-ipsa/is-plain-object]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object.</span>
-   <span class="signature">[`isPositiveZero( value )`][@patrtorg/quos-quasi-ipsa/is-positive-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to positive zero.</span>
-   <span class="signature">[`isPrime( value )`][@patrtorg/quos-quasi-ipsa/is-prime]</span><span class="delimiter">: </span><span class="description">test if a value is a prime number.</span>
-   <span class="signature">[`isPrimitive( value )`][@patrtorg/quos-quasi-ipsa/is-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript primitive.</span>
-   <span class="signature">[`isPRNGLike( value )`][@patrtorg/quos-quasi-ipsa/is-prng-like]</span><span class="delimiter">: </span><span class="description">test if a value is PRNG-like.</span>
-   <span class="signature">[`isProbability( value )`][@patrtorg/quos-quasi-ipsa/is-probability]</span><span class="delimiter">: </span><span class="description">test if a value is a probability.</span>
-   <span class="signature">[`isPropertyKey( value )`][@patrtorg/quos-quasi-ipsa/is-property-key]</span><span class="delimiter">: </span><span class="description">test whether a value is a property key.</span>
-   <span class="signature">[`isPrototypeOf( obj, prototype )`][@patrtorg/quos-quasi-ipsa/is-prototype-of]</span><span class="delimiter">: </span><span class="description">test if an object's prototype chain contains a provided prototype.</span>
-   <span class="signature">[`isReadOnlyPropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-read-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is read-only.</span>
-   <span class="signature">[`isReadOnlyProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-read-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is read-only.</span>
-   <span class="signature">[`isReadWritePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-read-write-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable and writable.</span>
-   <span class="signature">[`isReadWriteProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-read-write-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable and writable.</span>
-   <span class="signature">[`isReadablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-readable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable.</span>
-   <span class="signature">[`isReadableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-readable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable.</span>
-   <span class="signature">[`isRegExpString( value )`][@patrtorg/quos-quasi-ipsa/is-regexp-string]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression string.</span>
-   <span class="signature">[`isRelativePath( value )`][@patrtorg/quos-quasi-ipsa/is-relative-path]</span><span class="delimiter">: </span><span class="description">test if a value is a relative path.</span>
-   <span class="signature">[`isRelativeURI( value )`][@patrtorg/quos-quasi-ipsa/is-relative-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is a relative URI.</span>
-   <span class="signature">[`isSameComplex128( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-complex128]</span><span class="delimiter">: </span><span class="description">test if two arguments are both double-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameComplex64( v1, v2 )`][@patrtorg/quos-quasi-ipsa/is-same-complex64]</span><span class="delimiter">: </span><span class="description">test if two arguments are both single-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameNativeClass( a, b )`][@patrtorg/quos-quasi-ipsa/is-same-native-class]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same native class.</span>
-   <span class="signature">[`isSameType( a, b )`][@patrtorg/quos-quasi-ipsa/is-same-type]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same type.</span>
-   <span class="signature">[`isSameValueZero( a, b )`][@patrtorg/quos-quasi-ipsa/is-same-value-zero]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSameValue( a, b )`][@patrtorg/quos-quasi-ipsa/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSemVer( value )`][@patrtorg/quos-quasi-ipsa/is-semver]</span><span class="delimiter">: </span><span class="description">test if a value is a semantic version string.</span>
-   <span class="signature">[`isSlice( value )`][@patrtorg/quos-quasi-ipsa/is-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `Slice`.</span>
-   <span class="signature">[`isSnakecase( value )`][@patrtorg/quos-quasi-ipsa/is-snakecase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in snake case.</span>
-   <span class="signature">[`isStartcase( value )`][@patrtorg/quos-quasi-ipsa/is-startcase]</span><span class="delimiter">: </span><span class="description">test if a value is a startcase string.</span>
-   <span class="signature">[`isStrictEqual( a, b )`][@patrtorg/quos-quasi-ipsa/is-strict-equal]</span><span class="delimiter">: </span><span class="description">test if two arguments are strictly equal.</span>
-   <span class="signature">[`isTruthy( value )`][@patrtorg/quos-quasi-ipsa/is-truthy]</span><span class="delimiter">: </span><span class="description">test if a value is truthy.</span>
-   <span class="signature">[`isUNCPath( value )`][@patrtorg/quos-quasi-ipsa/is-unc-path]</span><span class="delimiter">: </span><span class="description">test if a value is a UNC path.</span>
-   <span class="signature">[`isUndefinedOrNull( value )`][@patrtorg/quos-quasi-ipsa/is-undefined-or-null]</span><span class="delimiter">: </span><span class="description">test if a value is undefined or null.</span>
-   <span class="signature">[`isUppercase( value )`][@patrtorg/quos-quasi-ipsa/is-uppercase]</span><span class="delimiter">: </span><span class="description">test if a value is an uppercase string.</span>
-   <span class="signature">[`isURI( value )`][@patrtorg/quos-quasi-ipsa/is-uri]</span><span class="delimiter">: </span><span class="description">test if a value is a URI.</span>
-   <span class="signature">[`isWhitespace( value )`][@patrtorg/quos-quasi-ipsa/is-whitespace]</span><span class="delimiter">: </span><span class="description">test whether a string contains only white space characters.</span>
-   <span class="signature">[`isWritablePropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-writable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is writable.</span>
-   <span class="signature">[`isWritableProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-writable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is writable.</span>
-   <span class="signature">[`isWriteOnlyPropertyIn( value, property )`][@patrtorg/quos-quasi-ipsa/is-write-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is write-only.</span>
-   <span class="signature">[`isWriteOnlyProperty( value, property )`][@patrtorg/quos-quasi-ipsa/is-write-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is write-only.</span>
-   <span class="signature">[`tools`][@patrtorg/quos-quasi-ipsa/tools]</span><span class="delimiter">: </span><span class="description">assertion utility tools.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var assert = require( '@patrtorg/quos-quasi-ipsa' );

console.log( objectKeys( assert ) );
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@patrtorg/quos-quasi-ipsa.svg
[npm-url]: https://npmjs.org/package/@patrtorg/quos-quasi-ipsa

[test-image]: https://github.com/patrtorg/quos-quasi-ipsa/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/patrtorg/quos-quasi-ipsa/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/patrtorg/quos-quasi-ipsa/main.svg
[coverage-url]: https://codecov.io/github/patrtorg/quos-quasi-ipsa?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/patrtorg/quos-quasi-ipsa.svg
[dependencies-url]: https://david-dm.org/patrtorg/quos-quasi-ipsa/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/patrtorg/quos-quasi-ipsa/tree/deno
[deno-readme]: https://github.com/patrtorg/quos-quasi-ipsa/blob/deno/README.md
[umd-url]: https://github.com/patrtorg/quos-quasi-ipsa/tree/umd
[umd-readme]: https://github.com/patrtorg/quos-quasi-ipsa/blob/umd/README.md
[esm-url]: https://github.com/patrtorg/quos-quasi-ipsa/tree/esm
[esm-readme]: https://github.com/patrtorg/quos-quasi-ipsa/blob/esm/README.md
[branches-url]: https://github.com/patrtorg/quos-quasi-ipsa/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/patrtorg/quos-quasi-ipsa/main/LICENSE

<!-- <toc-links> -->

[@patrtorg/quos-quasi-ipsa/contains]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/contains

[@patrtorg/quos-quasi-ipsa/deep-equal]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/deep-equal

[@patrtorg/quos-quasi-ipsa/deep-has-own-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/deep-has-own-property

[@patrtorg/quos-quasi-ipsa/deep-has-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/deep-has-property

[@patrtorg/quos-quasi-ipsa/has-own-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-own-property

[@patrtorg/quos-quasi-ipsa/has-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-property

[@patrtorg/quos-quasi-ipsa/has-utf16-surrogate-pair-at]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-utf16-surrogate-pair-at

[@patrtorg/quos-quasi-ipsa/instance-of]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/instance-of

[@patrtorg/quos-quasi-ipsa/is-absolute-http-uri]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-absolute-http-uri

[@patrtorg/quos-quasi-ipsa/is-absolute-path]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-absolute-path

[@patrtorg/quos-quasi-ipsa/is-absolute-uri]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-absolute-uri

[@patrtorg/quos-quasi-ipsa/is-accessor-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-accessor-property-in

[@patrtorg/quos-quasi-ipsa/is-accessor-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-accessor-property

[@patrtorg/quos-quasi-ipsa/is-alphagram]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-alphagram

[@patrtorg/quos-quasi-ipsa/is-alphanumeric]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-alphanumeric

[@patrtorg/quos-quasi-ipsa/is-anagram]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-anagram

[@patrtorg/quos-quasi-ipsa/is-arguments]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-arguments

[@patrtorg/quos-quasi-ipsa/is-arrow-function]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-arrow-function

[@patrtorg/quos-quasi-ipsa/is-ascii]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-ascii

[@patrtorg/quos-quasi-ipsa/is-between]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-between

[@patrtorg/quos-quasi-ipsa/is-bigint]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-bigint

[@patrtorg/quos-quasi-ipsa/is-binary-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-binary-string

[@patrtorg/quos-quasi-ipsa/is-blank-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-blank-string

[@patrtorg/quos-quasi-ipsa/is-boxed-primitive]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-boxed-primitive

[@patrtorg/quos-quasi-ipsa/is-buffer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-buffer

[@patrtorg/quos-quasi-ipsa/is-camelcase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-camelcase

[@patrtorg/quos-quasi-ipsa/is-capitalized]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-capitalized

[@patrtorg/quos-quasi-ipsa/is-circular]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-circular

[@patrtorg/quos-quasi-ipsa/is-class]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-class

[@patrtorg/quos-quasi-ipsa/is-collection]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-collection

[@patrtorg/quos-quasi-ipsa/is-composite]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-composite

[@patrtorg/quos-quasi-ipsa/is-configurable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-configurable-property-in

[@patrtorg/quos-quasi-ipsa/is-configurable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-configurable-property

[@patrtorg/quos-quasi-ipsa/is-constantcase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-constantcase

[@patrtorg/quos-quasi-ipsa/is-current-year]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-current-year

[@patrtorg/quos-quasi-ipsa/is-data-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-data-property-in

[@patrtorg/quos-quasi-ipsa/is-data-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-data-property

[@patrtorg/quos-quasi-ipsa/is-dataview]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-dataview

[@patrtorg/quos-quasi-ipsa/is-digit-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-digit-string

[@patrtorg/quos-quasi-ipsa/is-domain-name]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-domain-name

[@patrtorg/quos-quasi-ipsa/is-duration-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-duration-string

[@patrtorg/quos-quasi-ipsa/is-email-address]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-email-address

[@patrtorg/quos-quasi-ipsa/is-empty-collection]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-empty-collection

[@patrtorg/quos-quasi-ipsa/is-empty-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-empty-object

[@patrtorg/quos-quasi-ipsa/is-empty-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-empty-string

[@patrtorg/quos-quasi-ipsa/is-enumerable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-enumerable-property-in

[@patrtorg/quos-quasi-ipsa/is-enumerable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-enumerable-property

[@patrtorg/quos-quasi-ipsa/is-even]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-even

[@patrtorg/quos-quasi-ipsa/is-falsy]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-falsy

[@patrtorg/quos-quasi-ipsa/is-finite]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-finite

[@patrtorg/quos-quasi-ipsa/is-generator-object-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-generator-object-like

[@patrtorg/quos-quasi-ipsa/is-generator-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-generator-object

[@patrtorg/quos-quasi-ipsa/is-gzip-buffer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-gzip-buffer

[@patrtorg/quos-quasi-ipsa/is-hex-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-hex-string

[@patrtorg/quos-quasi-ipsa/is-infinite]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-infinite

[@patrtorg/quos-quasi-ipsa/is-inherited-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-inherited-property

[@patrtorg/quos-quasi-ipsa/is-iterable-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-iterable-like

[@patrtorg/quos-quasi-ipsa/is-iterator-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-iterator-like

[@patrtorg/quos-quasi-ipsa/is-json]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-json

[@patrtorg/quos-quasi-ipsa/is-kebabcase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-kebabcase

[@patrtorg/quos-quasi-ipsa/is-leap-year]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-leap-year

[@patrtorg/quos-quasi-ipsa/is-localhost]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-localhost

[@patrtorg/quos-quasi-ipsa/is-lowercase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-lowercase

[@patrtorg/quos-quasi-ipsa/is-method-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-method-in

[@patrtorg/quos-quasi-ipsa/is-method]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-method

[@patrtorg/quos-quasi-ipsa/is-multi-slice]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-multi-slice

[@patrtorg/quos-quasi-ipsa/is-named-typed-tuple-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-named-typed-tuple-like

[@patrtorg/quos-quasi-ipsa/is-native-function]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-native-function

[@patrtorg/quos-quasi-ipsa/is-negative-zero]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-negative-zero

[@patrtorg/quos-quasi-ipsa/is-node-builtin]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-builtin

[@patrtorg/quos-quasi-ipsa/is-node-duplex-stream-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-duplex-stream-like

[@patrtorg/quos-quasi-ipsa/is-node-readable-stream-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-readable-stream-like

[@patrtorg/quos-quasi-ipsa/is-node-repl]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-repl

[@patrtorg/quos-quasi-ipsa/is-node-stream-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-stream-like

[@patrtorg/quos-quasi-ipsa/is-node-transform-stream-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-transform-stream-like

[@patrtorg/quos-quasi-ipsa/is-node-writable-stream-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node-writable-stream-like

[@patrtorg/quos-quasi-ipsa/is-nonconfigurable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonconfigurable-property-in

[@patrtorg/quos-quasi-ipsa/is-nonconfigurable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonconfigurable-property

[@patrtorg/quos-quasi-ipsa/is-nonenumerable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonenumerable-property-in

[@patrtorg/quos-quasi-ipsa/is-nonenumerable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonenumerable-property

[@patrtorg/quos-quasi-ipsa/is-nonnegative-finite]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonnegative-finite

[@patrtorg/quos-quasi-ipsa/is-object-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-object-like

[@patrtorg/quos-quasi-ipsa/is-odd]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-odd

[@patrtorg/quos-quasi-ipsa/is-pascalcase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-pascalcase

[@patrtorg/quos-quasi-ipsa/is-plain-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-plain-object

[@patrtorg/quos-quasi-ipsa/is-positive-zero]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-positive-zero

[@patrtorg/quos-quasi-ipsa/is-prime]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-prime

[@patrtorg/quos-quasi-ipsa/is-primitive]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-primitive

[@patrtorg/quos-quasi-ipsa/is-prng-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-prng-like

[@patrtorg/quos-quasi-ipsa/is-probability]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-probability

[@patrtorg/quos-quasi-ipsa/is-property-key]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-property-key

[@patrtorg/quos-quasi-ipsa/is-prototype-of]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-prototype-of

[@patrtorg/quos-quasi-ipsa/is-read-only-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-read-only-property-in

[@patrtorg/quos-quasi-ipsa/is-read-only-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-read-only-property

[@patrtorg/quos-quasi-ipsa/is-read-write-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-read-write-property-in

[@patrtorg/quos-quasi-ipsa/is-read-write-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-read-write-property

[@patrtorg/quos-quasi-ipsa/is-readable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-readable-property-in

[@patrtorg/quos-quasi-ipsa/is-readable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-readable-property

[@patrtorg/quos-quasi-ipsa/is-regexp-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-regexp-string

[@patrtorg/quos-quasi-ipsa/is-relative-path]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-relative-path

[@patrtorg/quos-quasi-ipsa/is-relative-uri]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-relative-uri

[@patrtorg/quos-quasi-ipsa/is-same-complex128]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-complex128

[@patrtorg/quos-quasi-ipsa/is-same-complex64]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-complex64

[@patrtorg/quos-quasi-ipsa/is-same-native-class]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-native-class

[@patrtorg/quos-quasi-ipsa/is-same-type]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-type

[@patrtorg/quos-quasi-ipsa/is-same-value-zero]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-value-zero

[@patrtorg/quos-quasi-ipsa/is-same-value]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-value

[@patrtorg/quos-quasi-ipsa/is-semver]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-semver

[@patrtorg/quos-quasi-ipsa/is-slice]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-slice

[@patrtorg/quos-quasi-ipsa/is-snakecase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-snakecase

[@patrtorg/quos-quasi-ipsa/is-startcase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-startcase

[@patrtorg/quos-quasi-ipsa/is-strict-equal]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-strict-equal

[@patrtorg/quos-quasi-ipsa/is-truthy]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-truthy

[@patrtorg/quos-quasi-ipsa/is-unc-path]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-unc-path

[@patrtorg/quos-quasi-ipsa/is-undefined-or-null]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-undefined-or-null

[@patrtorg/quos-quasi-ipsa/is-uppercase]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uppercase

[@patrtorg/quos-quasi-ipsa/is-uri]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uri

[@patrtorg/quos-quasi-ipsa/is-whitespace]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-whitespace

[@patrtorg/quos-quasi-ipsa/is-writable-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-writable-property-in

[@patrtorg/quos-quasi-ipsa/is-writable-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-writable-property

[@patrtorg/quos-quasi-ipsa/is-write-only-property-in]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-write-only-property-in

[@patrtorg/quos-quasi-ipsa/is-write-only-property]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-write-only-property

[@patrtorg/quos-quasi-ipsa/tools]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/tools

[@patrtorg/quos-quasi-ipsa/has-arraybuffer-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-arraybuffer-support

[@patrtorg/quos-quasi-ipsa/has-arrow-function-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-arrow-function-support

[@patrtorg/quos-quasi-ipsa/has-async-await-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-async-await-support

[@patrtorg/quos-quasi-ipsa/has-async-iterator-symbol-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-async-iterator-symbol-support

[@patrtorg/quos-quasi-ipsa/has-bigint-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-bigint-support

[@patrtorg/quos-quasi-ipsa/has-bigint64array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-bigint64array-support

[@patrtorg/quos-quasi-ipsa/has-biguint64array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-biguint64array-support

[@patrtorg/quos-quasi-ipsa/has-class-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-class-support

[@patrtorg/quos-quasi-ipsa/has-dataview-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-dataview-support

[@patrtorg/quos-quasi-ipsa/has-define-properties-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-define-properties-support

[@patrtorg/quos-quasi-ipsa/has-define-property-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-define-property-support

[@patrtorg/quos-quasi-ipsa/has-float32array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-float32array-support

[@patrtorg/quos-quasi-ipsa/has-float64array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-float64array-support

[@patrtorg/quos-quasi-ipsa/has-function-name-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-function-name-support

[@patrtorg/quos-quasi-ipsa/has-generator-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-generator-support

[@patrtorg/quos-quasi-ipsa/has-globalthis-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-globalthis-support

[@patrtorg/quos-quasi-ipsa/has-int16array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-int16array-support

[@patrtorg/quos-quasi-ipsa/has-int32array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-int32array-support

[@patrtorg/quos-quasi-ipsa/has-int8array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-int8array-support

[@patrtorg/quos-quasi-ipsa/has-iterator-symbol-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-iterator-symbol-support

[@patrtorg/quos-quasi-ipsa/has-map-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-map-support

[@patrtorg/quos-quasi-ipsa/has-node-buffer-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-node-buffer-support

[@patrtorg/quos-quasi-ipsa/has-proxy-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-proxy-support

[@patrtorg/quos-quasi-ipsa/has-set-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-set-support

[@patrtorg/quos-quasi-ipsa/has-sharedarraybuffer-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-sharedarraybuffer-support

[@patrtorg/quos-quasi-ipsa/has-symbol-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-symbol-support

[@patrtorg/quos-quasi-ipsa/has-tostringtag-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-tostringtag-support

[@patrtorg/quos-quasi-ipsa/has-uint16array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-uint16array-support

[@patrtorg/quos-quasi-ipsa/has-uint32array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-uint32array-support

[@patrtorg/quos-quasi-ipsa/has-uint8array-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-uint8array-support

[@patrtorg/quos-quasi-ipsa/has-uint8clampedarray-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-uint8clampedarray-support

[@patrtorg/quos-quasi-ipsa/has-wasm-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-wasm-support

[@patrtorg/quos-quasi-ipsa/has-weakmap-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-weakmap-support

[@patrtorg/quos-quasi-ipsa/has-weakset-support]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/has-weakset-support

[@patrtorg/quos-quasi-ipsa/is-big-endian]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-big-endian

[@patrtorg/quos-quasi-ipsa/is-browser]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-browser

[@patrtorg/quos-quasi-ipsa/is-darwin]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-darwin

[@patrtorg/quos-quasi-ipsa/is-docker]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-docker

[@patrtorg/quos-quasi-ipsa/is-electron-main]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-electron-main

[@patrtorg/quos-quasi-ipsa/is-electron-renderer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-electron-renderer

[@patrtorg/quos-quasi-ipsa/is-electron]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-electron

[@patrtorg/quos-quasi-ipsa/is-little-endian]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-little-endian

[@patrtorg/quos-quasi-ipsa/is-mobile]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-mobile

[@patrtorg/quos-quasi-ipsa/is-node]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-node

[@patrtorg/quos-quasi-ipsa/is-touch-device]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-touch-device

[@patrtorg/quos-quasi-ipsa/is-web-worker]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-web-worker

[@patrtorg/quos-quasi-ipsa/is-windows]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-windows

[@patrtorg/quos-quasi-ipsa/is-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-error

[@patrtorg/quos-quasi-ipsa/is-eval-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-eval-error

[@patrtorg/quos-quasi-ipsa/is-range-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-range-error

[@patrtorg/quos-quasi-ipsa/is-reference-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-reference-error

[@patrtorg/quos-quasi-ipsa/is-syntax-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-syntax-error

[@patrtorg/quos-quasi-ipsa/is-type-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-type-error

[@patrtorg/quos-quasi-ipsa/is-uri-error]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uri-error

[@patrtorg/quos-quasi-ipsa/is-accessor-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-accessor-array

[@patrtorg/quos-quasi-ipsa/is-array-length]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-array-length

[@patrtorg/quos-quasi-ipsa/is-array-like-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-array-like-object

[@patrtorg/quos-quasi-ipsa/is-array-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-array-like

[@patrtorg/quos-quasi-ipsa/is-arraybuffer-view]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-arraybuffer-view

[@patrtorg/quos-quasi-ipsa/is-arraybuffer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-arraybuffer

[@patrtorg/quos-quasi-ipsa/is-between-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-between-array

[@patrtorg/quos-quasi-ipsa/is-bigint64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-bigint64array

[@patrtorg/quos-quasi-ipsa/is-biguint64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-biguint64array

[@patrtorg/quos-quasi-ipsa/is-circular-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-circular-array

[@patrtorg/quos-quasi-ipsa/is-empty-array-like-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-empty-array-like-object

[@patrtorg/quos-quasi-ipsa/is-empty-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-empty-array

[@patrtorg/quos-quasi-ipsa/is-falsy-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-falsy-array

[@patrtorg/quos-quasi-ipsa/is-finite-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-finite-array

[@patrtorg/quos-quasi-ipsa/is-numeric-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-numeric-array

[@patrtorg/quos-quasi-ipsa/is-plain-object-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-plain-object-array

[@patrtorg/quos-quasi-ipsa/is-probability-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-probability-array

[@patrtorg/quos-quasi-ipsa/is-same-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-array

[@patrtorg/quos-quasi-ipsa/is-same-complex128array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-complex128array

[@patrtorg/quos-quasi-ipsa/is-same-complex64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-complex64array

[@patrtorg/quos-quasi-ipsa/is-same-float32array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-float32array

[@patrtorg/quos-quasi-ipsa/is-same-float64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-same-float64array

[@patrtorg/quos-quasi-ipsa/is-sharedarraybuffer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-sharedarraybuffer

[@patrtorg/quos-quasi-ipsa/is-truthy-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-truthy-array

[@patrtorg/quos-quasi-ipsa/is-typed-array-length]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-typed-array-length

[@patrtorg/quos-quasi-ipsa/is-typed-array-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-typed-array-like

[@patrtorg/quos-quasi-ipsa/is-typed-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-typed-array

[@patrtorg/quos-quasi-ipsa/is-unity-probability-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-unity-probability-array

[@patrtorg/quos-quasi-ipsa/is-complex-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex-like

[@patrtorg/quos-quasi-ipsa/is-complex-typed-array-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex-typed-array-like

[@patrtorg/quos-quasi-ipsa/is-complex-typed-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex-typed-array

[@patrtorg/quos-quasi-ipsa/is-complex]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex

[@patrtorg/quos-quasi-ipsa/is-complex128]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex128

[@patrtorg/quos-quasi-ipsa/is-complex128array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex128array

[@patrtorg/quos-quasi-ipsa/is-complex64]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex64

[@patrtorg/quos-quasi-ipsa/is-complex64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex64array

[@patrtorg/quos-quasi-ipsa/is-centrosymmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-centrosymmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-complex128matrix-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex128matrix-like

[@patrtorg/quos-quasi-ipsa/is-complex128ndarray-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex128ndarray-like

[@patrtorg/quos-quasi-ipsa/is-complex128vector-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex128vector-like

[@patrtorg/quos-quasi-ipsa/is-complex64matrix-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex64matrix-like

[@patrtorg/quos-quasi-ipsa/is-complex64ndarray-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex64ndarray-like

[@patrtorg/quos-quasi-ipsa/is-complex64vector-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-complex64vector-like

[@patrtorg/quos-quasi-ipsa/is-float32matrix-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float32matrix-like

[@patrtorg/quos-quasi-ipsa/is-float32ndarray-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float32ndarray-like

[@patrtorg/quos-quasi-ipsa/is-float32vector-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float32vector-like

[@patrtorg/quos-quasi-ipsa/is-float64matrix-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float64matrix-like

[@patrtorg/quos-quasi-ipsa/is-float64ndarray-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float64ndarray-like

[@patrtorg/quos-quasi-ipsa/is-float64vector-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float64vector-like

[@patrtorg/quos-quasi-ipsa/is-matrix-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-matrix-like

[@patrtorg/quos-quasi-ipsa/is-ndarray-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-ndarray-like

[@patrtorg/quos-quasi-ipsa/is-nonsymmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonsymmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-persymmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-persymmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-skew-centrosymmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-skew-centrosymmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-skew-persymmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-skew-persymmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-skew-symmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-skew-symmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-square-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-square-matrix

[@patrtorg/quos-quasi-ipsa/is-symmetric-matrix]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-symmetric-matrix

[@patrtorg/quos-quasi-ipsa/is-vector-like]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-vector-like

[@patrtorg/quos-quasi-ipsa/is-float32array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float32array

[@patrtorg/quos-quasi-ipsa/is-float64array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-float64array

[@patrtorg/quos-quasi-ipsa/is-int16array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-int16array

[@patrtorg/quos-quasi-ipsa/is-int32array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-int32array

[@patrtorg/quos-quasi-ipsa/is-int8array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-int8array

[@patrtorg/quos-quasi-ipsa/is-uint16array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uint16array

[@patrtorg/quos-quasi-ipsa/is-uint32array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uint32array

[@patrtorg/quos-quasi-ipsa/is-uint8array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uint8array

[@patrtorg/quos-quasi-ipsa/is-uint8clampedarray]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-uint8clampedarray

[@patrtorg/quos-quasi-ipsa/is-cube-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-cube-number

[@patrtorg/quos-quasi-ipsa/is-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-integer-array

[@patrtorg/quos-quasi-ipsa/is-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-integer

[@patrtorg/quos-quasi-ipsa/is-negative-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-negative-integer-array

[@patrtorg/quos-quasi-ipsa/is-negative-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-negative-integer

[@patrtorg/quos-quasi-ipsa/is-negative-number-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-negative-number-array

[@patrtorg/quos-quasi-ipsa/is-negative-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-negative-number

[@patrtorg/quos-quasi-ipsa/is-nonnegative-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonnegative-integer-array

[@patrtorg/quos-quasi-ipsa/is-nonnegative-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonnegative-integer

[@patrtorg/quos-quasi-ipsa/is-nonnegative-number-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonnegative-number-array

[@patrtorg/quos-quasi-ipsa/is-nonnegative-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonnegative-number

[@patrtorg/quos-quasi-ipsa/is-nonpositive-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonpositive-integer-array

[@patrtorg/quos-quasi-ipsa/is-nonpositive-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonpositive-integer

[@patrtorg/quos-quasi-ipsa/is-nonpositive-number-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonpositive-number-array

[@patrtorg/quos-quasi-ipsa/is-nonpositive-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nonpositive-number

[@patrtorg/quos-quasi-ipsa/is-positive-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-positive-integer-array

[@patrtorg/quos-quasi-ipsa/is-positive-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-positive-integer

[@patrtorg/quos-quasi-ipsa/is-positive-number-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-positive-number-array

[@patrtorg/quos-quasi-ipsa/is-positive-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-positive-number

[@patrtorg/quos-quasi-ipsa/is-safe-integer-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-safe-integer-array

[@patrtorg/quos-quasi-ipsa/is-safe-integer]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-safe-integer

[@patrtorg/quos-quasi-ipsa/is-square-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-square-number

[@patrtorg/quos-quasi-ipsa/is-square-triangular-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-square-triangular-number

[@patrtorg/quos-quasi-ipsa/is-triangular-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-triangular-number

[@patrtorg/quos-quasi-ipsa/is-array-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-array-array

[@patrtorg/quos-quasi-ipsa/is-boolean-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-boolean-array

[@patrtorg/quos-quasi-ipsa/is-date-object-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-date-object-array

[@patrtorg/quos-quasi-ipsa/is-function-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-function-array

[@patrtorg/quos-quasi-ipsa/is-nan-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nan-array

[@patrtorg/quos-quasi-ipsa/is-null-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-null-array

[@patrtorg/quos-quasi-ipsa/is-number-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-number-array

[@patrtorg/quos-quasi-ipsa/is-object-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-object-array

[@patrtorg/quos-quasi-ipsa/is-string-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-string-array

[@patrtorg/quos-quasi-ipsa/is-symbol-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-symbol-array

[@patrtorg/quos-quasi-ipsa/is-array]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-array

[@patrtorg/quos-quasi-ipsa/is-boolean]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-boolean

[@patrtorg/quos-quasi-ipsa/is-date-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-date-object

[@patrtorg/quos-quasi-ipsa/is-function]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-function

[@patrtorg/quos-quasi-ipsa/is-nan]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-nan

[@patrtorg/quos-quasi-ipsa/is-null]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-null

[@patrtorg/quos-quasi-ipsa/is-number]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-number

[@patrtorg/quos-quasi-ipsa/is-object]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-object

[@patrtorg/quos-quasi-ipsa/is-regexp]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-regexp

[@patrtorg/quos-quasi-ipsa/is-string]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-string

[@patrtorg/quos-quasi-ipsa/is-symbol]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-symbol

[@patrtorg/quos-quasi-ipsa/is-undefined]: https://github.com/patrtorg/quos-quasi-ipsa/tree/main/is-undefined

<!-- </toc-links> -->

</section>

<!-- /.links -->
