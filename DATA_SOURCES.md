### Merchant Portfolio Query

The Merchant Portfolio query now includes the new field for merchant activation date.

```sql
SELECT
    m.MERCHANT_BUSINESS_CATEGORY,
    m.MERCHANT_ACTIVATION_DATE as activation_date,
    COUNT(*) as total_merchants,
    SUM(m.SOME_OTHER_FIELD) as total_value
FROM
    merchants m
WHERE
    m.ACTIVE = 1
GROUP BY
    m.MERCHANT_BUSINESS_CATEGORY, m.MERCHANT_ACTIVATION_DATE;
```