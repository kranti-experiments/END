# Session 3 Assignment
```bash
Write a function using only list filter lambda that can tell whether a number is a Fibonacci number or not. You can use a pre-calculated list/dict to store fab numbers till 10000 PTS:100
Using list comprehension (and zip/lambda/etc if required) write five different expressions that:

    add 2 iterables a and b such that a is even and b is odd
    strips every vowel from a string provided (tsai>>t s)
    acts like a ReLU function for a 1D array
    acts like a sigmoid function for a 1D array
    takes a small character string and shifts all characters by 5 (handle boundary conditions) tsai>>yxfn

A list comprehension expression that takes a ~200 word paragraph (write your own paragraph to check), and checks whether it has any of the swear words mentioned in https://github.com/RobertJGabriel/Google-profanity-words/blob/master/list.txt PTS:200
Using reduce functions:

    add only even numbers in a list
    find the biggest character in a string (printable ascii characters)
    adds every 3rd number in a list

Using randint, random.choice and list comprehensions, write an expression that generates 15 random KADDAADDDD number plates, where KA is fixed, D stands for a digit, and A stands for Capital alphabets. 10<<DD<<99 & 1000<<DDDD<<9999
Write the above again from scratch where KA can be changed to DL, and 1000/9999 ranges can be provided.
```

## Functions Overview

### list_filter_lambda_fibonacci_check
Input: Number
Output: True if the input number is fibonacci else False
Works only for the first 10000 Fibonacci numbers
```bash
Input: 8
Output: True
```

## Using List Comprehension

### add_iterables_even_odd
Input: 2 lists of numbers
Output: Addition of elements from list1 and list2 such that list1 element is even and list2 element is odd
```bash
Input: [1, 2, 3, 4] [1, 4, 5, 7]
Output: [6, 11]
```

### strip_vowels
Input: String
Output: Strip the vowels from input string
```bash
Input: "tsai"
Output: "ts""
```

### check_relu
Input: 1D array
Output: Ouput of relu activation function
```bash
Input: [-1, -0.98, 89, -98.78, 32]
Output: [0, 0, 89, 0, 32]
```

### check_sigmoid
Input: 1D array
Output: Ouput of sigmoid activation function
```bash
Input: [0.3373, 0.0101, -0.1856, -0.115, -0.7647]
Output: [0.5835, 0.5025, 0.4537, 0.4713, 0.3176]
```

### shift_chars
Input: String
Output: Shift each character in the input string by 5 characters
```bash
Input: "tsai"
Output: "yxfn"
```

### remove_swear_words
Input: Text/Paragraph
Output: Cleaned text after removing swear words
```bash
Input: "This is holy crap shi+"
Output: "This is holy"
```

## Using Reduce Function

### reduce_add_even_numbers
Input: List of numbers
Output: Sum of all the even numbers in the input list
```bash
Input: [1, 2, 3, 4, 5, 6, 7]
Output: 12 [2+4+6]
```

### reduce_find_biggest_character
Input: String
Output: Find bigger character in the input string
```bash
Input: "tsai"
Output: t
```

### reduce_add_every_third_number
Input: List of numbers
Output: Sum of every third number in the input list
```bash
Input: [1, 2, 3, 4, 5, 6, 7]
Output: 12 [1+4+7]
```


## Synthetic generation of vehicle numbers

### gen_number_plates
Input: None
Output: Generates vehicle numbers in the format KADDAADDDD
DD: Ranges from 10 to 99
DDDD: Ranges from 1000 to 9999
```bash
Input: None
Output: ['KA43IU4544', 'KA32MJ9484', ..]
```
### gen_number_plates_flexi
Input: state = "KA" or "DL"
Output: Generates vehicle numbers in the format KADDAADDDD
DDDD: Starting and Ending Ranges
```bash
Input: state="DL", dddd_start = 7898, dddd_end = 8967
Output: ['DL43IU8844', 'DL32MJ7989', ..]
```