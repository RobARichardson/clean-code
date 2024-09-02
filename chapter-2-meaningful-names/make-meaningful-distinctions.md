# Make Meaningful Distinctions

{% hint style="info" %}
Distinguish names in such a way that the reader knows what the differences offer.
{% endhint %}

1. It is not sufficient to add number series or noise words to satisfy the compiler. If names must be different, then they should also mean something.
2. Number-series naming (a1, a2, ...aN) is the opposite of intentional naming.
3. Noise words are a meaningless distinction (e.g. `Info` & `Data`)
4. Noise words are often redundant.
   1. The word `variable` should never appear in a variable name.
   2. The word `table` should never appears in a table name.

| Good          | Bad              |
| ------------- | ---------------- |
| `Customer`    | `CustomerInfo`   |
| `Money`       | `MoneyAmount`    |
| `Message`     | `TheMessage`     |
| `Product`     | `ProductData`    |
| `GetAccounts` | `GetAccountInfo` |
