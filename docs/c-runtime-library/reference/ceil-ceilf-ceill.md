---
title: "ceil, ceilf, ceill"
ms.date: "6/5/2020"
api_name: ["ceilf", "ceil", "ceill", "_o_ceil", "_o_ceilf"]
api_location: ["msvcrt.dll", "msvcr80.dll", "msvcr90.dll", "msvcr100.dll", "msvcr100_clr0400.dll", "msvcr110.dll", "msvcr110_clr0400.dll", "msvcr120.dll", "msvcr120_clr0400.dll", "ucrtbase.dll", "ntdll.dll", "api-ms-win-crt-math-l1-1-0.dll", "api-ms-win-crt-private-l1-1-0.dll"]
api_type: ["DLLExport"]
topic_type: ["apiref"]
f1_keywords: ["ceil", "ceilf", "ceill"]
helpviewer_keywords: ["calculating value ceilings", "ceill function", "ceil function", "ceilf function"]
ms.assetid: f4e5acab-5c8f-4b10-9ae2-9561e6453718
---
# ceil, ceilf, ceill

Calculates the ceiling of a value.

## Syntax

```C
double ceil(
   double x
);
float ceil(
   float x
);  // C++ only
long double ceil(
   long double x
);  // C++ only
float ceilf(
   float x
);
long double ceill(
   long double x
);
```

### Parameters

*x*<br/>
Floating-point value.

## Return Value

The **ceil** functions return a floating-point value that represents the smallest integer that is greater than or equal to *x*. There is no error return.

|Input|SEH Exception|Matherr Exception|
|-----------|-------------------|-----------------------|
|± **QNAN**, **IND**|none|**_DOMAIN**|

**ceil** has an implementation that uses Streaming SIMD Extensions 2 (SSE2). For information and restrictions about using the SSE2 implementation, see [_set_SSE2_enable](set-sse2-enable.md).

## Remarks

Because C++ allows overloading, you can call overloads of **ceil** that take **float** or **long** **double** types. In a C program, **ceil** always takes and returns a **double**.

By default, this function's global state is scoped to the application. To change this, see [Global state in the CRT](../global-state.md).

## Requirements

|Routine|Required header|
|-------------|---------------------|
|**ceil**, **ceilf**, **ceill**|\<math.h>|

For additional compatibility information, see [Compatibility](../../c-runtime-library/compatibility.md).

## Example

See the example for [floor](floor-floorf-floorl.md).

## See also

[Floating-Point Support](../../c-runtime-library/floating-point-support.md)<br/>
[floor, floorf, floorl](floor-floorf-floorl.md)<br/>
[fmod, fmodf](fmod-fmodf.md)<br/>
[round, roundf, roundl](round-roundf-roundl.md)<br/>
