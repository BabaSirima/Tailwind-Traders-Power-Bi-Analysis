# Tailwind Traders DAX Measures

This document contains the key DAX measures used in the Tailwind Traders Power BI Sales & Profit Analytics project.

## Median Sales

Calculates the median gross revenue in USD.

```DAX
Median Sales =
MEDIAN('Sales in USD'[Gross Revenue USD])
```

## Quarterly Profit

Calculates quarter-to-date net revenue using the Calendar table.

```DAX
Quarterly Profit =
TOTALQTD(
    SUM('Sales in USD'[Net Revenue USD]),
    'CalendarTable'[Date]
)
```

## Year-to-Date Profit

Calculates year-to-date net revenue using the Calendar table.

```DAX
Year-to-Date Profit =
TOTALYTD(
    SUM('Sales in USD'[Net Revenue USD]),
    'CalendarTable'[Date]
)
```

## Yearly Profit Margin

Calculates the ratio of gross revenue to net revenue.

```DAX
Yearly Profit Margin =
DIVIDE(
    SUM('Sales in USD'[Gross Revenue USD]),
    SUM('Sales in USD'[Net Revenue USD])
)
```
