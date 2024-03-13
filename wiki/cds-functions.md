# CDS Functions

## Annotations with @<
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_annotations_syntax.htm)

Annotations in a SELECT list of a CDS view can now be entered after an element. Before the name of an annotation, `@<` must be written instead of @.

## CONCAT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

Concatenates strings in arg1 and arg2. Trailing blanks in arg1, arg2, and in the result are ignored. The maximum length of the result is 1333.

## REPLACE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String arg1, in which all instances of arg2 are replaced by the content from arg3. The replacement of letters is case-sensitive. Trailing blanks are ignored in all arguments. The maximum length of the result is 1333

## ABS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

Absolute amount of arg.

## DIV
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

The result of a division of arg1 by arg2 is rounded to an integer. The sign is assigned after the amounts are divided; positive if the arguments have the same sign, and negative if the arguments have different signs. Exception: arg2 has the value 0.

## DIVISION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

Division of arg1 by arg2. The result is rounded to dec decimal places.

## FLOOR
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

Largest integer number not greater than the value of arg.

## MOD
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

Positive or negative integer remainder of the division of arg1 by arg2.

## ROUND
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_numeric_v1.htm)

Rounded value of arg. If pos is greater than 0, the value is rounded to the position pos on the right of the decimal separator. If this is not the case, position abs(pos)+1 to the left of the decimal separator is rounded. This results in a 0 if the number of places is not sufficient.

## COALESCE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_coalesce_expression_v1.htm)

`Coalesce` function in a SELECT statement of a CDS DDIC-based view (obsolete). Can be used to check whether arg1 contains a null value. In ABAP CDS, the coalesce function has two mandatory positional parameters, arg1 and arg2. It checks whether arg1 contains a null value. If yes, then it returns the value of arg2. If no, then it returns the value of arg1. If both arg1 and arg2 are null, then the null value is returned.

## UNIT_CONVERSION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_unit_curr_v1.htm)

Functions for converting between units and between currencies CDS DDIC-based view (obsolete). The functions have keyword parameters quantity, amount, ... (some of which are optional), to which actual parameters arg1, arg2, ... can or must be assigned when called using =>.

## CURRENCY_CONVERSION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_unit_curr_v1.htm#!ABAP_VARIANT_2@2@)

The function `CURRENCY_CONVERSION` performs a currency conversion for the value passed to the keyword parameter amount. The result has the data type CURR or DECFLOAT34 with the same technical properties as the actual parameter passed to amount. The currency conversion is performed on the basis of the client-dependent rules saved in the DDIC database tables TCUR... of package SFIB.

## DECIMAL_SHIFT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_unit_curr_v1.htm#!ABAP_VARIANT_3@3@)

The function `DECIMAL_SHIFT` sets the decimal separator of the value that is passed to the keyword parameter amount in accordance with a currency. The result has the data type CURR with the length 31 and 14 decimal places. Its value is produced by multiplying the input parameter rounded to two decimal places by 10 to the power of two minus the decimal places defined by the currency passed.

## CONCAT_WITH_SPACE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

Concatenates strings in arg1 and arg2 as with CONCAT. The number of blanks specified in spaces is inserted between arg1 and arg2. The maximum length of the result is 1333.

## INSTR
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

Position of the first occurrence of the string from sub in arg (case-sensitive). arg respects leading blanks and ignores trailing blanks. sub respects all blanks. sub must contain at least one character. If no occurrences are found, the result is 0.

## LEFT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String of the length len with the len left characters of arg (ignoring the trailing blanks). The value of len cannot be greater than the length of arg.

## LENGTH
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

Number of characters in arg ignoring trailing blanks.

## LTRIM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String with the content of arg in which all trailing blanks and leading characters are removed that match the character in char. A blank in char is significant.

## RIGHT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String of the length len with the len right characters of arg (ignoring the trailing blanks). The value of len cannot be greater than the length of arg.

## RPAD
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String of the length len with the left-aligned content of arg without trailing blanks and in which trailing blanks produced by the expanded string are replaced by the characters from the argument src (respecting all blanks). Leading blanks from arg are preserved. If more characters are required than exist in src, the content of src is used repeatedly. If len is less than the length of arg, it is truncated on the right. If src is empty and len is greater than the length of arg, arg remains unchanged.

## RTRIM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String with the content of arg in which all trailing blanks are removed and all trailing characters that match the character in char. A blank in char is significant.

## BINTOHEX
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_types_v1.htm#!ABAP_VARIANT_2A@2@)

`BINTOHEX` takes a byte string and converts it to a character string containing the half bytes of arg, converted to the hexadecimal characters 0 to 9 and A to F (left-aligned). The valid argument type is RAW with a maximum length of 255. The result has the type CHAR with twice the length of arg. Only fields of data sources can be specified as arguments.

## HEXTOBIN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_types_v1.htm#!ABAP_VARIANT_2B@3@)

`HEXTOBIN` converts a character string to a byte string whose half bytes are determined from the hexadecimal characters of arg. Any leading blanks are removed before the conversion from arg and all trailing blanks are then replaced by 0. The valid argument types are is CHAR or NUMC with a maximum length of 510. The result has the type RAW with half the length of arg. Only fields of data sources and literals can be specified as arguments.

## DATS_DAYS_BETWEEN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_5@5@)

The function `DATS_DAYS_BETWEEN` calculates the difference between two specified dates, date1 and date2, in days. The actual parameters must have the built-in data type DATS and should contain a valid date in the format YYYYMMDD. Any invalid dates specified are initialized or set to the value 00010101 before the calculation. The result has the data type INT4. If date2 is greater than date1, the result is positive. In the reverse case, it is negative.

## DATS_ADD_DAYS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_6@6@)

The function `DATS_ADD_DAYS` adds days days to a specified date date.

## DATS_ADD_MONTHS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_7@7@)

The function `DATS_ADD_MONTHS` adds months months to a specified date date.

## DATS_IS_VALID
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_4@4@)

The function `DATS_IS_VALID` determines whether date contains a valid date in the format YYYYMMDD. The actual parameter must have the built-in data type DATS. The result has the data type INT4.

## TIMS_IS_VALID
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_time_functions_v1.htm)

The function `TIMS_IS_VALID` determines whether time (if specified) contains a valid time in the format HHMMSS. The actual parameter must have the built-in data type TIMS. The result has the data type INT4.

## TSTMP_IS_VALID
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_4@4@)

The function `TSTMP_IS_VALID` determines whether an argument tstmp contains a valid time stamp in the format YYYYMMDDHHMMSS. The actual parameter must have the built-in data type DEC with length 15 and no decimal places. The result has the data type INT4.

## TSTMP_CURRENT_UTCTIMESTAMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_5@5@)

The function `TSTMP_CURRENT_UTCTIMESTAMP` returns a UTC time stamp in accordance with the POSIX standard. The result has the data type DEC with length 15 and no decimal places.

## TSTMP_SECONDS_BETWEEN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_6@6@)

The function `TSTMP_SECONDS_BETWEEN` calculates the difference between two specified time stamps, tstmp1 and tstmp2 in seconds. The actual parameter must have the built-in data type DEC with length 15 and no decimal places and contain valid time stamps in the format YYYYMMDDHHMMSS.

## TSTMP_ADD_SECONDS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_7@7@)

The function `TSTMP_ADD_SECONDS` adds seconds seconds to a time stamp tstmp. The actual parameter tstmp must have the built-in data type DEC with length 15 and no decimal places and contain a valid time stamp in the format YYYYMMDDHHMMSS.

## UPPER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String with a length of arg, in which all uppercase letters are transformed to lowercase letters.

## LOWER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v1.htm)

String with a length of arg, in which all lowercase letters were transformed to uppercase letters.

## ABAP_SYSTEM_TIMEZONE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timezone_functions_v1.htm#!ABAP_VARIANT_1@1@)

The function `ABAP_SYSTEM_TIMEZONE` returns the system time zone of the AS ABAP for the client specified with clnt. The actual parameter clnt must have the built-in dictionary type CLNT and must contain a valid client ID. The result has the CHAR type with a length of 6.

## ABAP_USER_TIMEZONE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timezone_functions_v1.htm#!ABAP_VARIANT_2@2@)

The function `ABAP_USER_TIMEZONE` returns the user time zone of the AS ABAP for the ABAP user specified with user and the client specified with clnt. The actual parameter user must have the built-in type CHAR. The same applies to the actual parameter clnt as to function ABAP_SYSTEM_TIMEZONE. The result has the CHAR type with a length of 6.

## TSTMP_TO_DATS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_1@1@)

The function `TSTMP_TO_DATS` extracts the local date for the time zone specified in tzone from a time stamp in the argument tstmp.

## TSTMP_TO_TIMS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_2@2@)

The function `TSTMP_TO_TIMS` extracts the local time for the time zone specified in tzone from a time stamp in the argument tstmp.

## TSTMP_TO_DST
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_3@3@)

The function `TSTMP_TO_DST` extracts the daylight saving time marker for the time zone specified in tzone from a time stamp in the argument tstmp. This is X if the time stamp for the time zone is in the daylight saving time, otherwise it is initial.

## DATS_TIMS_TO_TSTMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_4@4@)

The function `DATS_TIMS_TO_TSTMP` constructs a time stamp from a local date specified in date and a local time specified in time in the time zone specified in tzone. The daylight saving time is respected implicitly.

## FLTP_TO_DEC
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_types_v1.htm#!ABAP_VARIANT_1@1@)

Conversion of an argument arg of type FLTP to a packed number. Literals, fields of a data source data_source, and path expressions can be specified for arg. arg must have the type FLTP.

## IS INITIAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_cond_expr_initial_v1.htm)

The new condition `IS INITIAL` can be used to check the initial value of operands.

## DATN_DAYS_BETWEEN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_1@1@)

The function `DATN_DAYS_BETWEEN` calculates the difference between two specified dates, date1 and date2, in days. The actual parameters must have the built-in data type DATN and must contain a valid date in the format YYYYMMDD. The result has the data type INT4.

## DATN_ADD_DAYS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_2@2@)

The function `DATN_ADD_DAYS` adds days days to a specified date date.

## DATN_ADD_MONTHS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_functions_v1.htm#!ABAP_VARIANT_3@3@)

The function DATN_ADD_MONTHS adds months months to a specified date date.

## UTCL_CURRENT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_1@1@)

This function generates a UTC time stamp from the system time and the system date of AS ABAP in accordance with POSIX. The return value has the built-in dictionary type UTCLONG.

## UTCL_ADD_SECONDS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_2@2@)

The function `UTCL_ADD_SECONDS` adds seconds seconds to a time stamp utclong. It has two positional parameters. The actual parameter for the formal parameter utclong must have the built-in dictionary type UTCLONG and contain a valid UTC time stamp.

## UTCL_SECONDS_BETWEEN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_timestamp_functions_v1.htm#!ABAP_VARIANT_3@3@)

The function `UTCL_SECONDS_BETWEEN` calculates the difference between two specified time stamps, utcl1 and utcl2, in seconds. It has two positional parameters. The actual parameters for the formal parameters utcl1 and utcl2 must have the built-in dictionary type UTCLONG and contain a valid UTC time stamp.

## TSTMPL_TO_UTCL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_5@5@)

The function `TSTMPL_TO_UTCL` converts a time stamp tstmpl from the ABAP Dictionary type TIMESTAMPL to the built-in dictionary type UTCLONG.

## TSTMPL_FROM_UTCL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_6@6@)

The function `TSTMPL_FROM_UTCL` converts a time stamp utcl from the built-in dictionary type UTCLONG to the ABAP Dictionary type TIMESTAMPL. It is the counterpart to variant 5.

## DATS_TO_DATN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_7@7@)

The function `DATS_TO_DATN` converts a date dats from the built-in ABAP Dictionary data type DATS to the built-in ABAP Dictionary type DATN.

## DATS_FROM_DATN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_8@8@)

The function `DATS_FROM_DATN` converts a date date from the built-in ABAP Dictionary data type DATN to the built-in ABAP Dictionary type DATS.

## TIMS_TO_TIMN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_9@9@)

The function `TIMS_TO_TIMN` converts a time tims from the ABAP Dictionary type TIMS to the ABAP Dictionary type TIMN.

## TIMS_FROM_TIMN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_date_time_conversions_v1.htm#!ABAP_VARIANT_10@10@)

The function TIMS_FROM_TIMN converts a time time from the ABAP Dictionary type TIMN to the ABAP Dictionary type TIMS.

## REPLACE_REGEXPR
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_sql_functions_character_v2.htm)

A Perl Compatible Regular Expression (PCRE) pcre is replaced in arg1 with the character string specified in arg2. occ is optional and determines the number of occurrences of pcre to be replaced. By default, all occurrences are replaced.

## GET_NUMERIC_VALUE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_unit_curr_v2.htm#!ABAP_VARIANT_3@3@)

`GET_NUMERIC_VALUE` returns the numeric value of a currency or quantity field without its currency or unit key. arg must be a field of a data source. No other elementary operand, expression, or function is possible.

## CURR_TO_DECFLOAT_AMOUNT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_conv_func_unit_curr_v2.htm#!ABAP_VARIANT_4@4@)

The function `CURR_TO_DECFLOAT_AMOUNT` converts a currency field of data type CURR into a currency field of data type DECFLOAT34. arg must have data type CURR and a currency key must be assigned using the annotation Semantics.amount.currencyCode. The result has the data type DECFLOAT34 and exactly the same currency key that is assigned to arg must be assigned.

## SERIES_GENERATE_DATE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_series_generators.htm#@@ITOC@@ABENCDS_SERIES_GENERATORS_2)

The CDS table function `SERIES_GENERATE_DATE` creates a table with a series of dates.

## SERIES_GENERATE_INTEGER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_series_generators.htm#@@ITOC@@ABENCDS_SERIES_GENERATORS_3)

The CDS system entity `SERIES_GENERATE_INTEGER` creates a table with a series of numbers.

## SERIES_GENERATE_TIME
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_series_generators.htm#@@ITOC@@ABENCDS_SERIES_GENERATORS_4)

The CDS system entity `SERIES_GENERATE_TIME` creates a table with a series of times.

## SERIES_GENERATE_TIMESTAMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_series_generators.htm#@@ITOC@@ABENCDS_SERIES_GENERATORS_5)

The CDS table function `SERIES_GENERATE_TIMESTAMP` creates a table with a series of time stamps.

## CASE ELSE NULL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_case_expression_v2.htm)

In CDS view entities, the addition `ELSE NULL` is available in simple and complex case distinctions. It defines the null value as return value of the ELSE branch.