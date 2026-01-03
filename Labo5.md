Laboratory 5\
NONOGA Djintoba\
1032249064\

# First table

::: center
  --------- --------- ----------
  Country   Capital   language
  Togo      Lome      French
  Russia    Moscow    Russian
  Germany   Berlin    German
  --------- --------- ----------
:::

# Differnt Alignment

Now let's try different column alignments:

::: center
  Left Aligned    Centered    Right Aligned
  -------------- ---------- ---------------
  dog               meat             medium
  horse             hay               large
  frog             flies              small
  rabbit          carrots             small
  elephant         plants        very large
:::

# Too few items in a table row

what happens when we have too few items in a row:

::: center
  Animal   Food   Size
  -------- ------ -------
  dog      meat   
  horse    hay    large
  frog            
:::

**Observation:** Empty cells are created for missing items. The table still compiles but may look incomplete.

# Too many items in a table row

What happens when we have too many items:

**Observation:** LaTeX throws an error: `Extra alignment tab has been changed to \cr`. The compilation fails until the extra items are removed.

# Using `\multicolumn` 

Now let's experiment with column spanning:

::: center
+---------------+---------------+---------------+
| Animal        | Food          | Size          |
+:==============+:==============+:==============+
| dog           | meat          | medium        |
+---------------+---------------+---------------+
| Unknown Animal                | large         |
+---------------+---------------+---------------+
| horse         | Eats only hay (large)         |
+---------------+-------------------------------+
| All animals in this table are mammals         |
+---------------+---------------+---------------+
| frog          | flies         | small         |
+---------------+---------------+---------------+
:::

# Advanced Table features

## Custom column types

Using the `B` column type we defined for bold centered text:

:::: center
::: tabular
B p2cmr & Description & Size\
DOG & Loyal companion & medium\
CAT & Independent friend & small\
FISH & Aquatic creature & tiny\
:::
::::

## Numeric alignment with siunitx

Proper alignment of numeric data:

:::: center
::: tabular
S\[table-format=2.2\] S\[table-format=3.2\] Weight (kg) & Height (cm)\
& 45.20\
8.75 & 35.80\
25.00 & 62.30\
3.25 & 18.50\
15.80 & 52.10\
:::
::::

## Table with notes

Using `threeparttable` for footnotes:

::::: center
:::: threeparttable
  Animal     Diet          Lifespan
  ---------- ------------- --------------
  Dog        Omnivorous    10-13 years
  Cat        Carnivorous   12-15 years
  Tortoise   Herbivorous   80-150 years

::: tablenotes
Varies by breed and size

Some species can live even longer
:::
::::
:::::

## Column Styling

Styling columns with pre- and post-content:

::: center
  *:*        Food    Size
  ---------- ------- --------
  *dog :*    meat    medium
  *cat :*    fish    small
  *bird :*   seeds   tiny
:::

## Multi-page Table Example

A long table that can span multiple pages:

:::: center
::: longtable
llS\[table-format=2.1\]

\
Animal & Habitat & Avg Weight (kg)\
\
Animal & Habitat & Avg Weight (kg)\
African Elephant & Savanna & 6000.0\
Blue Whale & Ocean & 140000.0\
Giraffe & Savanna & 800.0\
Polar Bear & Arctic & 450.0\
Kangaroo & Outback & 25.0\
Penguin & Antarctica & 5.0\
Tiger & Jungle & 90.0\
Lion & Savanna & 100.0\
Gorilla & Rainforest & 160.0\
Eagle & Mountains & 1.5\
Dolphin & Ocean & 75.0\
Octopus & Ocean & 2.5\
Camel & Desert & 150.0\
Wolf & Forest & 40.0\
Fox & Various & 3.5\
Rabbit & Meadows & 0.5\
Squirrel & Forests & 0.2\
Bat & Caves & 0.02\
Hippopotamus & Rivers & 1500.0\
Rhinoceros & Savanna & 2300.0\
:::
::::

These skills form the foundation for creating professional, readable tables in scientific documents.
