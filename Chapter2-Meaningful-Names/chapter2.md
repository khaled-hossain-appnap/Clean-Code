# Meaningful Names

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

- <b> Choose names that reveal intent </b> <br>
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

- <b> Avoid Disinformation </b> </br>
  poor variable names

```
inch, cm, sec, accountList = {}
```

```
myAccountHolder, yourAccountHolder
```

- <b> Inconsistent Spelling </b>

```
accountInfo, acntInfo, acntInformation, accInfo
```

```
Product ProductInfo ProductData
```

```
moneyAmount, money, customerInfo, customer, accountData, account
```

- <b> Make Meaningful Distinctions. code for humans not for compiler. </b>

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

- <b> Avoid similar function names </b>

```
getActiveAccount();
getActiveAccounts();
getActiveAccountInfo();
```

- <b> Use Pronounceable Names. if you can't prnounce it you can not discuss it without sounding like an idiot. </b><br>
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

- <b> Use Searchable Names </b> <br>
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

- <b> Avoid Mental Mapping </b> <br>
  if you can reliably remember that r is the lower-cased version of the url with the host and scheme removed, then you must clearly be very smart.

- <b> Class Names </b> <br>
  classes and objects should have noun or noun phrase names like

```
Customer, WikiPage, Account, AddressParser
```

avoid

```
Manager, processor, Data, Info in the name of a class
```

a classname should not be a verb

- <b> Method Names</b> <br>
  Method names should have verb or verb names like

```
postPayment, deletePage, saveUser, getUser
```

It should prefixed by following keywords

```
get, set or action
```

- <b> for Boolean type value always use "is" prefix </b>

```
isLoading, setIsLoading, getIsLoading
```

- <b> Don't be Cute </b>

```
whack() to mean kill()
```

```
eatMyShorts() to mean abort()
```

```
holyHandGrenade() to mean deleteItems()
```

- <b> Pick One Word per Concept. Its confusing to use these keywords interchangably. </b>

```
fetch, retrieve, get
```

```
manager, controller, driver
```

- <b>Use Solution Domain Names </b></b>

```
AccountVisitor, NewsPublisher, JobQueue
```

- <b>Use Problem Domain Names </b>

```
BOGO, CouponDiscount, FreeDelivery
```

- <b>Add variable according to Context</b>

```
Address / PostAddress, Mac, URI
```
