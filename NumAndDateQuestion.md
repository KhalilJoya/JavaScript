# Questions

### 1 : How can you convert a string to a number in JavaScript? write all the ways.

```
      let str = "100.2";
      console.log(+str);

      console.log(Number(str));

      console.log(parseFloat(str));

      console.log(parseInt(str));

```

### 2 : How do you round a number to a certain number of decimal places in JavaScript?

```
  let num = 3.14159265;
  console.log(num.toFixed(2));

  console.log(Math.round(3.14159265));

```

### 3 : How can you generate a random number between two values in JavaScript?

```
   let min = 1;
   let max = 10;
   console.log(Math.floor(Math.random() * max) + min);

```

### 4 : How do you convert a number to a binary, octal, or hexadecimal format in JavaScript?

```
    let decimalNumber = 10;
    let binaryNumber = decimalNumber.toString(2);
    console.log(binaryNumber);

    let octalNumber = decimalNumber.toString(8);
    console.log(octalNumber);

    let hexNumber = decimalNumber.toString(16);
    console.log(hexNumber);

```

### 5 : How do you add or subtract a certain number of days from a date in JavaScript?

```
      let currentDate = new Date();
      let flusDate = new Date(currentDate.getTime() + 3 * 24 * 60 * 60 * 1000);

      let mainusDate = new Date(
        currentDate.getTime() - 2 * 24 * 60 * 60 * 1000
      );

      console.log(`Current Date :  ${currentDate}`);
      console.log(`+ 3 days : ${flusDate}`);
      console.log(`- 2 days : ${mainusDate}`);

```

### 6 : How do you compare two dates in JavaScript? Check if a date is small or large or equal to other date?

```
      let date1 = new Date("2023-04-10");
      let date2 = new Date("2023-05-15");
      if (date1 < date2) {
        console.log("date1 is earlier than date2");
      } else if (date1 > date2) {
        console.log("date1 is later than date2");
      } else {
        console.log("date1 and date2 are equal");
      }

```

### 7 : How can you format a date in JavaScript according to the user's locale?

```
      let date = new Date();
      let formattedDate = date.toLocaleDateString();
      console.log(`Formatted date : ${formattedDate}`);

```

### 8 : How do you calculate the difference between two dates in JavaScript?

```
      let date1 = new Date("2023-04-10");
      let date2 = new Date("2023-05-15");
      let differenceDate = date2.getTime() - date1.getTime();
      let differenceInDays = differenceDate / (1000 * 60 * 60 * 24);
      console.log(`Difference in days: ${differenceInDays}`);

```

### 9 : How do you check if a year is a leap year in JavaScript?

```
   

```

### 10 : How do you convert a string to a date in JavaScript? Write all ways.

```
      let dateString = "2023-04-05";
      let date = new Date(dateString);
      console.log(date);

```

### 11 : How can you parse a date from a string in a specific format in JavaScript?

```
      let dateString = "02/20/2023";
      let date = new Date(Date.parse(dateString));
      console.log(date);

```

### 12 : How can you get the time in a specific timezone in JavaScript?

```

```

### 13 : Print date and time after every 1 second in the format 'MM/DD/YYYY HH:MM:SS'

```
      function logDateTime() {
        let newDate = new Date();
        let date = newDate.toLocaleDateString("en-US");
        let time = newDate.toLocaleTimeString("en-US");
        console.log(`${date} ${time}`);
      }

      setInterval(logDateTime, 1000);

```

### 14 : Write a JavaScript function to get the number of days in a month. Pass month and year as an arugment to the function. for example : getDays(2, 2023). Answer will be 28

```
      function getDays(month, year) {
        return new Date(year, month, 0).getDate();
      }
      let ans = getDays(2, 2023);
      console.log(ans);

```

### 15 : Write a JavaScript function to get the week day name for the given date.

```
      function getWeekdayName(date) {
        let options = { weekday: "long" };
        return date.toLocaleString("en-US", options);
      }
      let date = new Date("2023-04-10");
      let weekday = getWeekdayName(date);
      console.log(weekday);

```

### 16 : Write a JavaScript function to get the month name from the given date

```
      function getMonthName(date) {
        let options = { month: "long" };
        return date.toLocaleString("en-US", options);
      }
      let date = new Date("2023-04-10");
      let month = getMonthName(date);
      console.log(month);

```

### 17 : Write a JavaScript function to check if given date is on weekend or not (Saturday/Sunday).

```
      function isWeekend(date) {
        let day = date.getDay();
        return day === 0 || day === 6;
      }
      let date1 = new Date("2023-04-08");
      let date2 = new Date("2023-04-09");
      let date3 = new Date("2023-04-10");
      console.log(isWeekend(date1));
      console.log(isWeekend(date2));
      console.log(isWeekend(date3));

```

### 18 : Ask your about his date of birth. Now write a JavaScript function to calculate age based on the given date of birth.

```

```

### 19 : Write a Javascript function to using setInterval to show alert box when date is your birth date.

```

```

### 20 : Show your birth date in Arabic

```
      let date = new Date("2003-09-30");
      options = {
        weekday: "long",
        year: "numeric",
        month: "short",
        day: "numeric",
      };
      let dateString = date.toLocaleDateString("ar-SA", options);
      console.log(dateString);

```

### 21 : Show your birth date in Chinese

```
      let date = new Date("2003-09-30");
      options = {
        weekday: "long",
        year: "numeric",
        month: "short",
        day: "numeric",
      };
      let dateString = date.toLocaleDateString("zh-cn", options);
      console.log(dateString);

```

### 22 : Write a JavaScript function to convert a binary number to a decimal number.

```

```

### 23 : Write a JavaScript function to convert a decimal number to binary, hexadecimal or octal number.

```
      function convert(number, base) {
        if (base === 2) {
          return number.toString(2);
        } else if (base === 8) {
          return number.toString(8);
        } else if (base === 16) {
          return number.toString(16);
        } else {
          return null;
        }
      }
      console.log(convert(10, 2));
      console.log(convert(10, 8));
      console.log(convert(10, 16));
      console.log(convert(10, 3));

```

### 24 : Write a JavaScript function to find the highest value in an array using Math.max

```
      function highestValue(arr) {
        if (arr.length === 0) {
          return null;
        }
        return Math.max(...arr);
      }
      console.log(highestValue([1, 2, 50, 3, 4, 5]));

```

### 25 : Write a JavaScript function to find the highest value in an array using Math.min

```
      function lowestValue(arr) {
        if (arr.length === 0) {
          return null;
        }
        return Math.min(...arr);
      }
      console.log(lowestValue([1, 2, 50, 3, 4, 5]));

```

### 26 : Write a JavaScript function to check whether a value is an integer or not.

```

```

### 27 : Write a JavaScript function to convert a positive number to negative number or to negativie number to positive number.

```
      function toggleSign(number) {
        return -number;
      }
      console.log(toggleSign(5));
      console.log(toggleSign(-5));

```

### 28 : Convert 50 litre to Hindi locale and chinese locale

```
   console.log(
        new Intl.NumberFormat("zh-cn", {
          style: "unit",
          unit: "liter",
          unitDisplay: "long",
        }).format(50)
      );

```

### 29 : Create a function to convert any number to given currency.

```
      function convertToCurrency(number, currency) {
        return new Intl.NumberFormat("en-US", {
          style: "currency",
          currency: currency,
        }).format(number);
      }
      console.log(convertToCurrency(10000.2, "USD"));
      console.log(convertToCurrency(10000.2, "EUR"));
      console.log(convertToCurrency(10000.2, "INR"));

```

### 30 : Write a JavaScript program to find the missing number from a given array. There are no duplicates in the list. Start from 1

```

```
