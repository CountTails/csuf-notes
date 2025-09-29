# Lecture 6: decision table based testing

## Definition

- Formally known as specification-based unit, decision table-based testing
- Not restricted to unit testing only
- Examples here will focus on the unit testing aspects

## An ATM example

> A customer requests a cash withdrawal. One of the business rules for the ATM is that the ATM machine pays out the amount if the customer has sufficient funds in their account or if the customer has the credit granted. Already, this simple example of a business rule is quite complicated to
describe in text

- Already, this simple example of a business rule is quite complicated to describe in text
- A decision table can make the same requirements easier to understand

| Conditions | R1 | R2 | R3 |
| ---------- | -- | -- | -- |
| Withdrawal amount <= balance | T | F | F |
| Credit granted | - | T | F |
| **Actions** | | | |
| Withdrawal granted | T | T | F |

### The decision table

- Conditions are usually expressed as true (T) or false (F)
- Columns correspond to the business logic that describe unique combinations of circumstances that will result in the actions
- It is normal to create at least 1 test case per column, which results in full coverage of all business rules

**Advantages**

- Makes it possible to detect combinations of conditions that would otherwise not be found
- Requirements can become clearer and often reveals some are illogical

**Disadvantages**

- Not equivalent to complete test cases containing step-by-step instructions of what to do in what order
- This more abstract level of detail often has to be further detailed into test cases

## An e-commerce application example (handling of credit cards)

**Possible inputs**

- Is the account real?
- Is the account active?
- Is the amount request within the credit limit?
- Is the consumer spending location okay?

**Possible outcomes**

- The charging request is approved
- Need to call cardholder (to verify)
- Need to call vendor (maybe to get more information or call policy)

**How many business rules?**

- 4 inputs becomes 16 combinations of inputs

| Conditions | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
| ---------- | - | - | - | - | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- |
| Real account? | Y | Y | Y | Y | Y | Y | Y | Y | N | N | N | N | N | N | N | N |
| Active account? | Y | Y | Y | Y | N | N | N | N | Y | Y | Y | Y | N | N | N | N |
| Within limit? | Y | Y | N | N | Y | Y | N | N | Y | Y | N | N | Y | Y | N | N |
| Location okay? | Y | N | Y | N | Y | N | Y | N | Y | N | Y | N | Y | N | Y | N |
| **Actions** | | | | | | | | | | | | | | | | |
| Approve? | Y | N | N | N | N | N | N | N | N | N | N | N | N | N | N | N |
| Call cardholder? | N | Y | Y | Y | N | Y | Y | Y | N | N | N | N | N | N | N | N |
| Call vendor? | N | N | N | N | Y | Y | Y | Y | Y | Y | Y | Y | Y | Y | Y | Y |

**How do actions affect the number of columns**

- Collapsed decision table only shows the 7 condition combinations that matter

| Conditions | 1 | 2 | 3 | 5 | 6 | 7 | 9 |
| ---------- | - | - | - | - | - | - | - |
| Real account? | Y | Y | Y | Y | Y | Y | N |
| Active account? | Y | Y | Y | N | N | N | - |
| Within limit? | Y | Y | N | Y | Y | N | - |
| Location okay? | Y | N | - | Y | N | - | - |
| **Actions** | | | | | | | |
| Approve? | Y | N | N | N | N | N | N |
| Call cardholder? | N | Y | Y | N | Y | Y | N |
| Call vendor? | N | N | N | Y | Y | Y | Y |
