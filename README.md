# vanguard-balance-fetcher
Get the balance of [Vanguard](https://investor.vanguard.com) accounts

# usage

```js
import fetchBalance from 'vanguard-balance-fetcher';

const securityQuestionAnswers = [
  {
    question: 'What is the first name of your boy or girlfriend?',
    answer: 'Katy'
  },
  {
    question: 'What is the last name of your first boss?',
    answer: 'Kim'
  },
  ...
];


fetchBalance('username', 'password', securityQuestionAnswers, (err, balance) => {
  if (err) {
    // TODO Handle error
    return;
  }

  console.log(balance);
});
```

## And the `balance` looks like this:
```js
{
  AccountID1: {
    VABCD: 1000.00,
    VZXYP: 952.12
  },
  AccountID2: {
    VXXXX: 1234.00
  },
  ...
}
```

# Caveats

* Due to the nature of what the library does, the function may not be working as intend
whenever the website changes. Please file an issue or create a pull request for the fix if the library doesn't work.

# License

[WTFPL](http://www.wtfpl.net)
