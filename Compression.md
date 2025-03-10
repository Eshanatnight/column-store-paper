# Compression

Compression techniques are employed by columnar databases
to decrease storage demands and enhance query performance.
There are several ways in which they achieve this:

1. Dictionary encoding: This technique uses a dictionary to store unique values
   for a column and replaces the original values with shorter codes.
   This results in a reduction of the storage space necessary to store data,
   particularly for columns that possess a high cardinality.
2. Run-length encoding: This technique stores repeated values in a column as a
   single value and count pair.
   For example, if a column has 1000 consecutive values of 'A',
   it can be stored as 'A-1000'. This technique is especially effective for columns
   with long runs of repeated values.
3. Bit-packing: This technique stores multiple values in a single machine word,
   reducing the amount of space needed to store the data.
   For example, if a column contains boolean values, each value can be stored as
   a single bit, instead of a full byte.
4. Delta encoding: This technique stores the difference between adjacent values
   in a column, instead of the actual values. This is useful for columns with
   sequential data, such as dates or timestamps.

By using these compression techniques, columnar databases can significantly
reduce storage requirements and improve query performance,
making them well-suited for analytical workloads.
