# Transpose operator

## Inner Product
### Reference
- https://en.wikipedia.org/wiki/Inner_product_space

### Definition

        < X, Y >  = < [x1; x2; ...; xn], [y1; y2; ...; yn] >,  

                  = [x1; x2; ...; xn]' * [y1; y2; ...; yn],  

                  = SUM_(i=1)^(n) xi * yi,   

                  = (x1 * y1) + (x2 * y2) + ... + (xn * yn).

## Complex conjugate
### Reference
- https://en.wikipedia.org/wiki/Complex_conjugate
 
### Definition
        (a + ib)' = (a - ib).

## Transpose
### Reference
- http://en.wikipedia.org/wiki/Transpose

### Definition
If `A` satisfies the following relation,   

        < A * X, Y > = < X, AT * Y >,  

then,

        AT is transpose of A.
        
### Examples
#### (1) [2D matrix](http://en.wikipedia.org/wiki/Transpose)

If `A` is defined as follow,

        A in R ^ (M, N),

then,

        AT in R ^ (N, M).
---
#### (2) [Differential function](https://en.wikipedia.org/wiki/Differential_operator)

If `A(x)` is  defined as follow,

        A(x) = x(i+1) - x(i),
        
then `AT(y)` is that,

        AT(y) = y(i) - y(i+1).
---
#### (3) [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform)

If `A(x)` is Fourier transform,

        A(x) = fftn(x)/numel(x),

then `AT(y)` is Inverse Fourier transform,
          
        AT(y) = ifftn(y).
---
#### (4) [Radon transform](https://en.wikipedia.org/wiki/Radon_transform) 

If `A(x)` is Radon transform called by `'Projection'`,

        A(x) = radon(x, THETA)
        
        where, THETA is degrees vector.
        
then `AT(y)` is Inverse Radon transform without Filtration called by `'Backprojection'`, 

        AT(y) = iradon(y, THETA, 'none', N)/(pi/(2*length(THETA))).
        
        where, 'none' is filtration option and N is image size. 
        
