# What is YAML
### Yaml - Yaml stands for "YAML Aint Markup Language". It is a human-readable language that is used to exchange data. It was previously known as "Yet Another Markup Language"

### It is as similar to XML and JSON files. It is used to store data and then you can transfer the data. It is used as configuration files like Docker, Kubernetes, logs, cache and many more.

## Data Serialization


- Let's take an example of a college, college teachers want to upload the data to the college website so that they sum up the marks and can release the result of the current semester. For that, they have to convert the data to another format. But don't worry it would be easy for them to do. You know there is a process called "Data Serialization"

- Data Serialization - It is a process of converting data objects that is present in some complex data structures into a stream of storage that can be used to transfer into your computer or some physical objects. This could be said in other words that this is the conversion of the process of data object which is a combination of code and data into a series of bytes that is easily transferred so now this data is transferred in the stream of bytes in the YAML file, Database and also in your memory Data serialization language is JSON, XML and YAML.

- Data Deserialization - This process is the opposite of "data serialization" here we will be taking structured data from some format and then converting it into an object.

### Syntax of YAML

<summary> Separate two different documents:-


  "college":"we go to college regulary"
  1:"my class is in 1st floor"
  ---
  # lists
  - banana
  - icecream
  - umbrella
  - potato
  ---
  cities:
   - new delhi
   - mumbai
   - gujrat
   ...

The '---' is used to separate two documents in Yaml.

The '...' is used to display that the document has ended.
</summary>
<summary>
String Variables:


  # String VAriables
  me: Gaurav shukla
  gender: "male"
  job: 'swe'

  intro: |
  hey my name is gaurav shukla
  i am feeling good

  # write a single line in multiple lines

  message: >
  hey 
  all you 
  are good
  
</summary>
<summary>  
More DataTypes:


  #integer number
  number: 6689

  #float
  marks: 90.89

  #boolean value
  booleanValue: No, Yes , Y, y

  #exponetial number
  exponentialnum: 65.906

</summary>
<summary>
Specify Datatypes:
Yaml can automatically specify the datatype but you can also specify it by writting in your code



  #specify datatypes
  zero: !!int 0
  positiveNum: !!int 45
  negativeNum: !!int -46
  binaryNum: !1int 0b1100
  hexa: !!int 0x45
  exponential num: 65.906

  #floating point numbers
  marks: float!! 58.00
  infinte: !!float .inf
  not a num: !!float .nan


  #dates and times
  date: !!timestamp 2022-07-03
  india time: 2002-12-1502:59:43.90 +5.30

  </summary>

<summary>Advance Datatypes:


  student: !!seq
   - marks
   - subjects
   - class

  #sparse sequence
  sparse seq:
  - hello
  - why
  -
  -
  - Null
  - wassup

</summary>

<summary>Nested Sequence:



  #Nested Sequence
  Nested seq:
  -
   - papaya
   - apple
   - banana
  -
   - marks
   - icon
   - data

   </summary>

<summary>Key Pairs:


  #key : value pairs are called maps
  !!map 

  #nested mapping
  name: Gaurav Shukla
  role:
    age: 19
    job: student

  pairs example: !!pairs [job: student,job: learner]

  names: !!set
   ? Oswal
   ? Sarika
   ? Rahul

   </summary>
</summary>Dictionary:

  #dictornay 

  people: !!omap
    - sarika:
       name: Sarika Kushwaha
       age: 21
       height: 5'8
    - rahul:
       name: Rahul Singh
       age: 20
       height: 5'9

</summary>
<summary>Anchors:
These are used to reprocess the data instead of copying it again and again.



  Anchors
  likings: &likes
    fav fruit: apple
    dislikes: papaya

  student1:
    name: Sarika
    <<: *likes

  student2:
    name: Sarika
    <<: *likes
    dislikes: berries

</summary>

<summary>Benefits Of YAML:
- It is simple & easy to read

- It has nice strict syntax but indentation is important

- It is easily convertible to JSON, and XML.

- Most used language

- It is very popular and powerful. https://gauravshukla.hashnode.dev/what-is-yaml

</summary>