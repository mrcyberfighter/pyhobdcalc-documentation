
:mod:`pyhobdcalc` -- Python Hexadecimal Octal Binar Decimal Calculator.
=======================================================================

.. module:: pyhobdcalc

:platform: Linux.

:synopsis: Conversion and calculating functions set for bases 2, 8, 10 and 16, written in C.

.. moduleauthor:: Eddie Bruggemann <mrcyberfighter@gmail.com>

++++++++++++++++++++++++++
Base conversion functions:
++++++++++++++++++++++++++

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Different bases integer strings conversion to integer:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~   

********
bintoint
********

.. function:: bintoint(binar_string)
    
    
    Take an binar integer string as argument and return the converted value as an integer string.
    
    The binar string must be in form: [-][0b][01] (the \"0b\" identifier is optional). 
    
        * Maximal represented value:  9223372036854775807. 
    
        * Minimal represented value: -9223372036854775808. 
    
        Corresponding to the C type: :c:type:`long long int`
    
    :raise OverflowError: If the binar string represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the binar string is not in the format: [-][0b][01].
    
********
octtoint
********   
    
.. function:: octtoint(octal_string)
    
    
    Take an octal integer string as argument and return the converted value as an integer string.
    
    The octal string must be in form: [-][0][0-7] (the \"0\" identifier is optional). 
    
        * Maximal represented value:  9223372036854775807. 
    
        * Minimal represented value: -9223372036854775808. 
    
        Corresponding to the C type: :c:type:`long long int`
    
    :raise OverflowError: If the octal string represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the octal string is not in the format: [-][0][0-7].    
    
********
hextoint
********    
    
    
.. function:: hextoint(hexadecimal_string)
    
    
    Take an hexadecimal integer string as argument and return the converted value as an integer string.
    
    The hexadecimal string must be in form: [-][0x][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
        * Maximal represented value:  9223372036854775807. 
    
        * Minimal represented value: -9223372036854775808. 
    
        Corresponding to the C type: :c:type:`long long int`
    
    :raise OverflowError: If the hexadecimal string represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the hexadecimal string is not in the format: [-][0x][0-9A-Fa-f].
    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 
Different bases floats strings conversion to floats: 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

***************
binfloattofloat
***************

.. function:: binfloattofloat(binar_string) 

    Take a binar float string as argument and return the converted value as an float string. 
    
    The binar string must be in form: [-][0b][01][.][01] (the \"0b\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    
    :raise OverflowError: If the binar string integer part represent an value greater as 9223372036854775807 or littler as -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the binar string is not in the format: [-][0b][01].[01].
  
***************
octfloattofloat
***************  
    
.. function:: octfloattofloat(octal_string) 

    Take a octal float string as argument and return the converted value as an float string. 
    
    The octal string must be in form: [-][0][0-7][.][0-7] (the \"0\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    
    
    :raise OverflowError: If the octal string integer part represent an value greater as 9223372036854775807 or littler as -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the octal string is not in the format: [-][0][0-7][.][0-7]. 
   
***************
hexfloattofloat 
***************   
   
    
.. function:: hexfloattofloat(hexadecimal_string) 

    Take a hexadecimal float string as argument and return the converted value as an float string. 
    
    The hexadecimal string must be in form: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    
    :raise OverflowError: If the hexadecimal string integer part represent an value greater as 9223372036854775807 or littler as -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError:    If the hexadecimal string is not in the format: [-][0x][0-9A-Fa-f].[0-9A-Fa-f].       
    
+++++++++++++++++++++++++++++++++++++++++++++
Base 2, 8, 16 integers calculating functions:
+++++++++++++++++++++++++++++++++++++++++++++

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Binar integer calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    
*********
binaddbin
*********
    
.. function:: binaddbin(binstr1,binstr2)

    Take 2 binar integer string as input return the summe as an integer string. 
    
    The binar strings must be in form: [-][0b][01] (the \"0b\" identifier is optional). 
    
        * Addition maximal result value: 9223372036854775807.
    
        * Addition minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the binar strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the binar strings addition result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].
    
*********
binsubbin
*********
    
.. function:: binsubbin(binstr1,binstr2)

    Take 2 binar integer string as input return the substract as an integer string. 
    
    The binar strings must be in form: [-][0b][01] (the \"0b\" identifier is optional). 
    
        * Substraction maximal result value: 9223372036854775807.
    
        * Substraction minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the binar strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the binar strings substraction result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].
    
**********
binmultbin
**********
    
.. function:: binmultbin(binstr1,binstr2)

    Take 2 binar integer string as input return the product as an integer string. 
    
    The binar strings must be in form: [-][0b][01] (the \"0b\" identifier is optional). 
    
        * Product maximal result value: 9223372036854775807.
    
        * Product minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the binar strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the binar strings product result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].
    
*********
bindivbin
*********
    
.. function:: bindivbin(binstr1,binstr2)

    Take 2 binar integer string as input return the quotient as an float string. 
    
    The binar strings must be in form: [-][0b][01] (the \"0b\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the binar strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the binar strings quotient result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
       
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].       
    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Octal integer calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    
*********
octaddoct
*********
    
.. function:: octaddoct(octstr1,octstr2)

    Take 2 octal integer string as input return the summe as an integer string. 
    
    The octal strings must be in form: [-][0][0-7] (the \"0\" identifier is optional). 
    
        * Addition maximal result value: 9223372036854775807.
    
        * Addition minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the octal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the octal strings addition result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].
    
*********
octsuboct
*********
    
.. function:: octsuboct(octstr1,octstr2)

    Take 2 octal integer string as input return the substract as an integer string. 
    
    The octal strings must be in form: [-][0][0-7] (the \"0\" identifier is optional). 
    
        * Substraction maximal result value: 9223372036854775807.
    
        * Substraction minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the octal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the octal strings substraction result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].
    
**********
octmultoct
**********
    
.. function:: octmultoct(octstr1,octstr2)

    Take 2 octal integer string as input return the product as an integer string. 
    
    The octal strings must be in form: [-][0][0-7] (the \"0\" identifier is optional). 
    
        * Product maximal result value: 9223372036854775807.
    
        * Product minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the octal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the octal strings product result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].
    
*********
octdivoct
*********
    
.. function:: octdivoct(octstr1,octstr2)

    Take 2 octal integer string as input return the quotient as an float string. 
    
    The octal strings must be in form: [-][0][0-7] (the \"0\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the octal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the octal strings quotient result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
       
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].       
    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Hexadecimal integer calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    
*********
hexaddhex
*********
    
.. function:: hexaddhex(hexstr1,hexstr2)

    Take 2 hexadecimal integer string as input return the summe as an integer string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
        * Addition maximal result value: 9223372036854775807.
    
        * Addition minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the hexadecimal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the hexadecimal strings addition result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f].
    
*********
hexsubhex
*********
    
.. function:: hexsubhex(hexstr1,hexstr2)

    Take 2 hexadecimal integer string as input return the substract as an integer string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
        * Substraction maximal result value: 9223372036854775807.
    
        * Substraction minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the hexadecimal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the hexadecimal strings substraction result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f].
    
**********
hexmulthex
**********
    
.. function:: hexmulthex(hexstr1,hexstr2)

    Take 2 hexadecimal integer string as input return the product as an integer string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
        * Product maximal result value: 9223372036854775807.
    
        * Product minimal result value: -9223372036854775808.
    
    :raise OverflowError: If the hexadecimal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the hexadecimal strings product result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f].
    
*********
hexdivhex
*********
    
.. function:: hexdivhex(hexstr1,hexstr2)

    Take 2 hexadecimal integer string as input return the quotient as an float string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the hexadecimal strings represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise OverflowError: If the hexadecimal strings quotient result is greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int` 
       
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f].        
        
+++++++++++++++++++++++++++++++++++++++++++
Base 2, 8, 16 floats calculating functions:
+++++++++++++++++++++++++++++++++++++++++++

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Binar float calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*******************
binfloataddbinfloat
*******************

.. function:: binfloataddbinfloat(binstr1,binstr2)

    Take 2 binar float string as input return the summe as an float string. 
    
    The binar strings must be in form: [-][0b][01].[01] (the \"0b\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire binar string can contains 128 binary digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the binar strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].[01].
 
*******************
binfloatsubbinfloat
******************* 
 
.. function:: binfloatsubbinfloat(binstr1,binstr2)

    Take 2 binar float string as input return the substract as an float string. 
    
    The binar strings must be in form: [-][0b][01].[01] (the \"0b\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire binar string can contains 128 binary digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the binar strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].[01].
 
********************
binfloatmultbinfloat
******************** 
 
.. function:: binfloatmultbinfloat(binstr1,binstr2)

    Take 2 binar float string as input return the product as an float string. 
    
    The binar strings must be in form: [-][0b][01].[01] (the \"0b\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire binar string can contains 128 binary digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the binar strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].[01].  
  
*******************
binfloatdivbinfloat
*******************  
  
.. function:: binfloatdivbinfloat(binstr1,binstr2)

    Take 2 binar float string as input return the quotient as an float string. 
    
    The binar strings must be in form: [-][0b][01].[01] (the \"0b\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire binar string can contains 128 binary digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the binar strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the binar strings are not in the format: [-][0b][01].[01]. 
    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Octal float calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*******************
octfloataddoctfloat
*******************

.. function:: octfloataddoctfloat(octstr1,octstr2)

    Take 2 octal float string as input return the summe as an float string. 
    
    The octal strings must be in form: [-][0][0-7].[0-7] (the \"0\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire octal string can contains 48 octal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the octal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].[0-7].
 
*******************
octfloatsuboctfloat
******************* 
 
.. function:: octfloatsuboctfloat(octstr1,octstr2)

    Take 2 octal float string as input return the substract as an float string. 
    
    The octal strings must be in form: [-][0][0-7].[0-7] (the \"0\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire octal string can contains 48 octal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the octal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].[0-7].
 
********************
octfloatmultoctfloat
******************** 
 
.. function:: octfloatmultoctfloat(octstr1,octstr2)

    Take 2 octal float string as input return the product as an float string. 
    
    The octal strings must be in form: [-][0][0-7].[0-7] (the \"0\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire octal string can contains 48 octal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the octal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].[0-7].  
  
*******************
octfloatdivoctfloat
*******************  
  
.. function:: octfloatdivoctfloat(octstr1,octstr2)

    Take 2 octal float string as input return the quotient as an float string. 
    
    The octal strings must be in form: [-][0][0-7].[0-7] (the \"0\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire octal string can contains 48 octal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the octal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the octal strings are not in the format: [-][0][0-7].[0-7].            
        
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Hexadecimal float calculating functions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*******************
hexfloataddhexfloat
*******************

.. function:: hexfloataddhexfloat(hexstr1,hexstr2)

    Take 2 hexadecimal float string as input return the summe as an float string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire hexadecimal string can contains 16 hexadecimal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the hexadecimal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f].
 
*******************
hexfloatsubhexfloat
******************* 
 
.. function:: hexfloatsubhexfloat(hexstr1,hexstr2)

    Take 2 hexadecimal float string as input return the substract as an float string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire hexadecimal string can contains 16 hexadecimal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the hexadecimal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f].
 
********************
hexfloatmulthexfloat
******************** 
 
.. function:: hexfloatmulthexfloat(hexstr1,hexstr2)

    Take 2 hexadecimal float string as input return the product as an float string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire hexadecimal string can contains 16 hexadecimal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the hexadecimal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f].  
  
*******************
hexfloatdivhexfloat
*******************  
  
.. function:: hexfloatdivhexfloat(hexstr1,hexstr2)

    Take 2 hexadecimal float string as input return the quotient as an float string. 
    
    The hexadecimal strings must be in form: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f] (the \"0x\" identifier is optional). 
    
    The function can threads 8 bytes values for the integer part from the float, in the C type :c:type:`long long int` value range:
    
        * Maximal integer part value:  9223372036854775807.
    
        * Minimal integer part value: -9223372036854775808.
        
    The entire hexadecimal string can contains 16 hexadecimal digits (without identifier, sign and comma.). 
    
    The returned result is limited to the C type :c:type:`double`: 15 digits precision. But the module compute internally with the C type :c:type:`long double`.
    
    :raise OverflowError: If the hexadecimal strings integer part represent an value greater than 9223372036854775807 or littler than -9223372036854775808.
    
    Corresponding to the range of the C type: :c:type:`long long int`
    
    :raise ValueError: If the hexadecimal strings are not in the format: [-][0x][0-9A-Fa-f][.][0-9A-Fa-f].     
    
    
    

  
    
                 
        
    
    
             
