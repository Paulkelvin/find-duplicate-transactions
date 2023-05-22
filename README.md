# Finding Duplicate Transaction in financial systems

Sometimes when a customer is charged, there is a duplicate transaction created. We need to find those transactions so that they can be dealt with. Everything about the transaction should be identical, except the transaction `id` and the `time` at which it occurred, as there can be up to a minute delay.

The code finds all transactions that have the same `sourceAccount`, `targetAccount`, `category`, `amount`, and the `time` difference between each consecutive transaction is less than 1 minute and put them in groups.

### Input

An array of transaction objects, with an `id`, `sourceAccount`, `targetAccount`, `amount`, `category`, and `time`. You can assume that all parameters will always be present and valid. However, the incoming transactions are not guaranteed to be in any particular order.

### Output

A list of all the duplicate transaction groups, ordered by time ascending. The groups should be sorted in ascending order of the first transaction in the group.
