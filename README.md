# KGMatrix

###Written by Kevin Gay in Python 2.7!
###Link to Git: https://github.com/KevinGay/KGMatrix

This module creates a matrix data structure and provides methods to perform common matrix operations. The name of
the algorithm is the method name if a specific algorithm is used.

	Note: operator overloading has been implemented so the following is possible:

    	    -Addition/subtraction between two matrices
		
	    -Multiplication/division between two matrices
		
        	    OR
						
             between a matrix and a scalar as long as the scalar follows the matrix.
	     
###Testing	

		Two functions have been included below for testing: test1 checks operator overloading and the methods
		for solving a matrix, while test2 checks the more advanced algorithms for finding eigenvectors and
		eigenvalues. Check the implementation for more specific detail. The correct outputs have been posted
		on the GitHub page.
        
        
#Help on Matrix in module \__main__ object:

##   Methods defined here:
   
   QR(self)
   
       Use the QR Method to find all of the eigenvalues and eigenvectors of a matrix.
   
   \__add__(self, other)
   
       Operator overloading for matrix addition.
   
   \__div__(self, other)
   
       If other is a matrix, perform matrix division.
       If other is an int or float: return the result of scaling the matrix by 1 / other.
       
       Conditions:
 
               -if input is a scalar, it must be an int or a float.
                        **SCALAR MUST COME AFTER MATRIX IN EXPRESSION**
 
               -if input is a matrix, the first matrix rows must match the
                        second matrix columns.
                                
       Resultant matrix of mult(m x n, n x p) will always be m x p.
   
   \__init__(self, matrixList=[])
   
       Creates a matrix using a supplied list.
       If no list is supplied, assume the matrix is empty.
       matrixList: list of floats or ints.
   
   \__mul__(self, other)
   
       If other is a matrix, perform matrix multiplication
       if other is a scalar, multiply each item in the matrix by a scalar.
       
       Conditions:
       
           -if input is a scalar, it must be an int or a float
               **SCALAR MUST COME AFTER MATRIX IN EXPRESSION**
       
           -if input is a matrix, the first matrix rows must match the
               second matrix columns.
       
       Resultant matrix of mult(m x n, n x p) will always be m x p.
   
   \__sub__(self, other)
   
       Operator overloading for matrix subtraction.
   
   asList(self)
   
       Make a copy of the matrix and store it in list form.
       Mostly for use in methods of self.
   
   augment(self, b)
   
       Augment the current matrix with a solution vector b.
       pre: b must be a one-dimensional list.
   
   covariance(self)
   
       Return the covariance matrix of the current matrix.
   
   det(self)
   
       Returns the determinant of a matrix.
   
   gaussJordan(self)
   
       Uses Gauss Jordan method of elimination to reduce current matrix.
   
   gaussian(self)
   
       Use gaussian elimination to reduce current matrix.
   
   getColumnSumNorm(self)
   
       Get the norm of a matrices in the form of a column sum norm.
   
   getColumnVector(self, column)
   
       Return one of the columns as a matrices.
   
   getRowSumNorm(self)
   
       Get the norm of a matrices in the form of a row sum norm.
   
   identity(self, n)
   
       Returns an n x n identity matrix.
   
   importMatrix(self, file)
   
       Imports a matrix from a file and returns it.
       Pre: file must exist and be a valid file.
   
   inverse(self)
   
       Find the inverse of a matrix by reducing the given matrix to the identity,
       the starting identity matrix becomes the inverse.
   
   leverrier(self)
   
       Use Leverrier's method to fid the characteristic polynomial of a matrix.
   
   meanVector(self)
   
       Return an nx1 matrix of the mean column vectors of a matrix.
   
   powerMethod(self, y)
   
       Use the power method to find the largest eigenvalue of a matrix.
   
   ref(self)
   
       Returns the row echelon form (not reduced).
   
   toString(self, roundTo=3)
   
       Prints the matrix out in a clean format.
       roundTo is an optional parameter which specifies how many decimals to round to.
       It is recommended to keep roundTo at 3 unless you change the value in the string formatting.
   
   trace(self)
   
       Calculate the trace of the matrix.
   
   transpose(self)
   
       Return the transpose of a matrix.
   
   upperTriangularTest(self, B)
   
       Determines if a matrix is upper triangular or not.
   
   zeroes(self, m, n=-1)
   
       Returns an m x n matrix of all zeroes.
   
  ----------------------------------------------------------------------
