# Assignment-110

Shape relates to the size of the dimensions of an N-dimensional array.

Size regarding arrays, relates to the amount (or count) of elements that are contained in the array (or sometimes, at the top dimension of the array - when used as length).

For example, let a be a matrix

1  2  3  4
5  6  7  8
9 10 11 12
the shape of a is (3, 4), the size of a is
 12 and the size of a[1] is 4.

The term broadcasting refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations. Arithmetic operations on arrays are usually done on corresponding elements. If two arrays are of exactly the same shape, then these operations are smoothly performed.

Example 1
Live Demo
import numpy as np 

a = np.array([1,2,3,4]) 
b = np.array([10,20,30,40]) 
c = a * b 
print c
Its output is as follows −

[10   40   90   160]
If the dimensions of two arrays are dissimilar, element-to-element operations are not possible. However, operations on arrays of non-similar shapes is still possible in NumPy, because of the broadcasting capability. The smaller array is broadcast to the size of the larger array so that they have compatible shapes.

Broadcasting is possible if the following rules are satisfied −

Array with smaller ndim than the other is prepended with '1' in its shape.

Size in each dimension of the output shape is maximum of the input sizes in that dimension.

An input can be used in calculation, if its size in a particular dimension matches the output size or its value is exactly 1.

If an input has a dimension size of 1, the first data entry in that dimension is used for all calculations along that dimension.

A set of arrays is said to be broadcastable if the above rules produce a valid result and one of the following is true −

Arrays have exactly the same shape.

Arrays have the same number of dimensions and the length of each dimension is either a common length or 1.

Array having too few dimensions can have its shape prepended with a dimension of length 1, so that the above stated property is true.

The following program shows an example of broadcasting.
One of the key features of Python is its numerous libraries and packages. In this article, we will list down the popular packages and libraries in Python that are being widely used for numeric and scientific applications.

(The list is in no particular order).

1| SciPy (Scientific Numeric Library)
Officially released in 2000-01, SciPy is free and open source library used for scientific computing and technical computing. The library consists of modules for optimisation,

image processing, FFT, special functions and signal processing.

The SciPy package includes algorithms and functions which are the crux of Python scientific computing capabilities. The sub-package includes: 

  io: used for the standard input and output
lib: this function is used to wrap python external libraries
signal: used for processing signal tools
sparse: used for algorithms related to sparse matrix
spatial: widely used to determine paths in KD-trees, nearest neighbor and distance functions.
optimise: used to optimise algorithms which include linear programming.
linals: used for the regular linear algebra applications.
interpolate: used for the integration of tools
intergate: applied for integration of numerical tools
fftpack: this subpackage helps for the discretion Fourier to transform algorithms
cluster: the package consists of hierarchical clustering, vector quantisation, and K-means.
misc: used for the miscellaneous utility applications.
special: used to switch in special functions.
weave: a tool to convert C/C++ codes to python programming.
ndimage: used for wide range of functions in multi-dimensional image processing.
stats: used for better understanding and analysing of statistical functions.
constants: this algorithm includes physical specification and conversion components.
2| Pandas (Data Analytics Library.

NumPy introduces a simple file format for ndarray objects. This .npy file stores data, shape, dtype and other information required to reconstruct the ndarray in a disk file such that the array is correctly retrieved even if the file is on another machine with different architecture.

numpy.save()
The numpy.save() file stores the input array in a disk file with npy extension.

import numpy as np 
a = np.array([1,2,3,4,5]) 
np.save('outfile',a)
To reconstruct array from outfile.npy, use load() function.

import numpy as np 
b = np.load('outfile.npy') 
print b 
It will produce the following output −

array([1, 2, 3, 4, 5])
The save() and load() functions accept an additional Boolean parameter allow_pickles. A pickle in Python is used to serialize and de-serialize objects before saving to or reading from a disk file.

savetxt()
The storage and retrieval of array data in simple text file format is done with savetxt() and loadtxt() functions.

Example
import numpy as np 

a = np.array([1,2,3,4,5]) 
np.savetxt('out.txt',a) 
b = np.loadtxt('out.txt') 
print b 
It will produce the following output −

[ 1.  2.  3.  4.  5.] 
The savetxt() and loadtxt() functions accept additional optional parameters such as header, footer, and delimiter.

The numpy module of Python provides a function called numpy.empty(). This function is used to create an array without initializing the entries of given shape and type.

Just like numpy.zeros(), the numpy.empty() function doesn't set the array values to zero, and it is quite faster than the numpy.zeros(). This function requires the user to set all the values in the array manually and should be used with caution.

Syntax
numpy.empty(shape, dtype=float, order='C')  
Parameters:
shape: int or tuple of ints

This parameter defines the shape of the empty array, such as (3, 2) or (3, 3).

dtype: data-type(optional)

This parameter defines the data type, which is desired for the output array.

order: {'C', 'F'}(optional)

This parameter defines the order in which the multi-dimensional array is going to be stored either in row-major or column-major. By default, the order parameter is set to 'C'.

Returns:
This function returns the array of uninitialized data that have the shape, dtype, and order defined in the function.





