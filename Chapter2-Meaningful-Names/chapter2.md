# Chapter 2 - Meaningful Names

## Use Intention-Revealing Names

Bad

```
int d; // elapsed time in days
```

Good

```
int elapsedTimeInDays;
int daysSinceCreation;
int daysSinceModification;
int fileAgeInDays;
```

## Choose names that reveal intent

BAD

```
getThem() {
  const list1 = [];
  const x = [];

  for (let i=0; i<list1.length; i++){
    if(x[0] == 4) {
      list1.push(x[i])
    }
  }

  return list1;
}
```

Good

```
getFlaggedCells() {
  const flaggedCells = [];

  for (int cell in gameBoard) {
    if(cell.isFlagged()) {
      flaggedCells.push(gameBoard[cell])
    }
  }

  return flaggedCells;
}
```

## Avoid Disinformation

poor variable names

```
inch, cm, sec, accountList = {}
```

```
myAccountHolder, yourAccountHolder
```

## Inconsistent Spelling

```
accountInfo, acntInfo, acntInformation, accInfo
```

```
Product ProductInfo ProductData
```

```
moneyAmount, money, customerInfo, customer, accountData, account
```

## Make Meaningful Distinctions.

code for humans not for compiler

```
copyChars(a1[], a2[]){
  for (let i=0; i < a1.length; i++){
    a2[i] = a1[i]
  }
}
```

we could use source and destination as arguments.

```
NameString, CustomerObject
```

## Avoid similar function names

```
getActiveAccount();
getActiveAccounts();
getActiveAccountInfo();
```

## Use Pronounceable Names.

if you can't prnounce it you can not discuss it without sounding like an idiot.<br>
Bad

```
class DtaRcrd102 {
  int gynymdhms;
  int modymdhms
  pszqint
}

```

Good

```
class Customer {
int generationTimestamp;
int modificationTimestamp
int recordId
}
```

## Use Searchable Names

Bad

```
for(int j=0; j<34; j++){
  s += (t[j] * 4) / 5;
}
```

Good

```
int realDaysPerIdealDay = 4;
const WORK_DAYS_PER_WEEK = 5;
int sum = 0;

for (int j=0; j< NUMBER_OF_TASKS; j++) {
  int realTaskDays = taskEstimate[j] * realDaysPerIdealDay;
  int realTaskWeeks = (realDays / WORK_DAYS_PER_WEEK)
  sum += realTaskWeeks;
}
```

## Avoid Mental Mapping

if you can reliably remember that r is the lower-cased version of the url with the host and scheme removed, then you must clearly be very smart.

## Class Names

classes and objects should have noun or noun phrase names like

```
Customer, WikiPage, Account, AddressParser
```

avoid

```
Manager, processor, Data, Info in the name of a class
```

a classname should not be a verb

## Method Names

Method names should have verb or verb names like

```
postPayment, deletePage, saveUser, getUser
```

It should prefixed by following keywords

```
get, set or action
```

## for Boolean type value always use "is" prefix

```
isLoading, setIsLoading, getIsLoading
```

## Don't be Cute

```
whack() to mean kill()
```

```
eatMyShorts() to mean abort()
```

```
holyHandGrenade() to mean deleteItems()
```

## Pick One Word per Concept.

Its confusing to use these keywords interchangably

```
fetch, retrieve, get
```

```
manager, controller, driver
```

## Use Solution Domain Names

```
AccountVisitor, NewsPublisher, JobQueue
```

## Use Problem Domain Names

```
BOGO, CouponDiscount, FreeDelivery
```

## Add variable according to Context

```
Address / PostAddress, Mac, URI
```
