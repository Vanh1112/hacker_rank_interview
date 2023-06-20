# **NOTE:** To ensure fairness and accuracy for each applicant, all of your actions will be tracked via webcam; do not open another tab, and and the copy feature has been disabled.

1. Find the Sequence In a game, there is a string, direction, of length n that consists of characters L and R. L denotes left, R denotes right, and there is a line segment of length 2^n that extends from [0, 2^n], a player takes n turns.

In the ith turn,

* The player places the number i at the center of the current line segment.

* If direction[i] = 'L', the player proceeds in the left direction, eliminating the right half of the current line segment, and vice versa for direction[i] = 'R'.   Following this rule, find the final order of numbers on the line segment, starting from the left.

**Example:**

 **direction = "LRRLLL"**

 There are n = 6 characters in the initial length of the line segment. The segment length is 2^n = 2^6 = 64 in the range [0, 64].
 The game proceeds as follows:

|Center|Number|Direction|Remaining Segment|
|------|------|---------|-----------------|
|      |      |         |[ 0, 64]         |
|32    |1     |L        |[ 0, 32]         |
|16    |2     |R        |[16, 32]         |
|24    |3     |R        |[24, 32]         |
|28    |4     |L        |[24, 28]         |
|26    |5     |L        |[24, 26]         |
|25    |6     |L        |[24, 25]         |


 The smallest center point is 16 and the value placed is 2. The next smaller center is 24 with a value of 3. When the centers are ordered ascending, their values are [2, 3, 6, 5, 4, 1].

**Function Description:**

 Complete the function findNumberSequence in the editor below.
 findNumberSequence has the following parameter:
 string direction: a string of length n where each character denotes the direction of a turn

**Returns:**

 int[n] : an integer array that denotes the indices of characters in the string ordered by placement point
 Constraints 1 ≤ n ≤ 10^5 The string direction consists of 'L' or 'R' only.


------------------------------------------------------------------------------------------------------------------------------------------------------------------

 2. Two tables are provided that contains people's names, their current and previous employers. First determine the company or companies that have the highest number of people that were previously employed there. For all of the people who work at one of those companies currently, list the person's name and the name of their previous employer. Results should be in the form people.NAME companies.NAME.  The order of the results is not important.

**There are 2 tables:** PEOPLE, COMPANIES. PEOPLE
Name Type Description

ID STRING ID of the person.

NAME STRING Name of the person.

DOJ DATE Date of Joining the current company.

PREV_COMPANY_ID STRING ID of the previous company.



3. Given the dataset of schools and the subjects they offer as a pandas dataframe, perform the following operations: Drop all the schools offering fewer than 3 subjects. Clean the 'state_code' column such that it only contains alpha-numeric characters. For each state, return the number of schools offering English, Maths, Physics and Chemistry, each in a separate column.

The given dataframe consists of three columns:
school_id - School ID for each student state_code - Unique identifier for each state subjects - space-separated strings of subjects, all in lowercase   Consider, for example, you are given the following dataframe:

|    | school_id   | state_code   | subjects                       |
|---:|:------------|:-------------|:-------------------------------|
|  0 | sch_1       | !@sc_1       | english maths chemistry        |
|  1 | sch_2       | ))sc_2       | english physics chemistry      |
|  2 | sch_3       | !@sc_2       | maths biology fine_art         |
|  3 | sch_4       | sc_2)_       | french                         |
|  4 | sch_5       | sc_1#@       | social_studies maths literature|
|  5 | sch_6       | sc_10#@      | english maths history          |
|  6 | sch_7       | sc_3@!#$@    | biology geography              |
|  7 | sch_8       | sc_12##     | english physics                |



 **After performing the steps:**

|state_code|english|maths|physics|chemistry|
|----------|-------|-----|-------|---------|
|sc1       |1      |2    |0      |1        |
|sc10      |1      |1    |0      |0        |
|sc2       |1      |0    |1      |1        |

 Function Description Complete the function stateCount in the editor below.   stateCount has the following parameter(s):
 * **df:** a pandas dataframe

**Returns**

 pandas dataframe: the results of processing

 Constraints 1 ≤ number of rows in df ≤ 1000

 ------------------------------------------------------------------------------------------------------------------------------------------------------------------

 4. Find Longest Ride Given the dataset of taxi rides completed in a pandas dataframe,

**process the dataframe as follows:**
Drop all the rows where the pickup time or dropoff time is missing.
Find the longest ride (on basis of duration) for each pickup month (YYYY-MM). Sort the resulting dataframe by the pickup month.

**The given dataframe consists of four columns:**
id - unique trip id vendor_id - vendor id pickup_datetime - when the ride started dropoff_datetime - when the ride ended.

Consider, for example, you are given the following dataframe:

|id |vendor_id                    |pickup_datetime|dropoff_datetime                             |
|---|-----------------------------|---------------|---------------------------------------------|
|id01234|3                            |2016-06-06 06:06:20| 2016-06-06 08:00:00                         |
|id01434|4                            |2016-06-09 06:06:20|2016-06-09 06:07:20                          |
|id13234|3                            |2016-07-06 03:06:10 |                                             |


**After performing the steps:**

|pickup_month|id                           |
|------------|-----------------------------|
|2016-06     |id01234                      |


Function Description Complete the function longestRide in the editor below.   longestRide has the following parameter(s):
* df:  a pandas dataframe

**Constraints**

pandas dataframe: the results of processing df

Constraints 1 ≤ the number of rows in the dataframe ≤ 1000.

It is guaranteed that the resulting dataframe consists of at least one row with no nulls.

CURR_COMPANY_ID STRING ID of the current company.

COMPANIES Name Type Description ID STRING ID of the company.

NAME STRING Name of the company.

------------------------------------------------------------------------------------------------------------------------------------------------------------------


5. Write a python script for calculate veloccity record in below table, then choose unrealistic velocity record and send us your python script:



|id|lat 1 |long 1 |lat 2|long 2|time (hour)|
|---|---|-----------------------------|---------------|---------------------------------------------|----|
A|42.60503444|-85.65985058 |42.62415889| -85.B6224915| 3|
C|42.28574388| -83.41309542| 41.06767655| -85.66224915| 8 |
D|40.71608837| -74.03154507| 40.70771506| -74.01793887| 0.5|
E|43.58947598| -84.73793251| 43.59759173| -84.73800983| 3|
F|39.954077|	-74.235622 |13.463678| -116.849280|2|
G|41.574040|	-87.453100 | 36.554230|	-58.181500|6|

the unrealistic velocity record are:



*   A
*   B
*   C
*   D
*   E
*   G
*   A & B
*   E & G

------------------------------------------------------------------------------------------------------------------------------------------------------------------

6. In NLP, stop words are commonly used words like "a", "is", and "the". They are typically filtered out during processing.   Implement a function that takes a string text and an integer k, and returns the list of words that occur in the text at least k times. The words must be returned in the order of their first occurrence in the text.   Example text = "a mouse is smaller than a dog but a dog is stronger" k=2   The list of stop words that occur at least k = 2 times is ["a", "is", "dog"]. "a" occurs 3 times, "is" and "dog" both occur 2 times. No other word occurs at least 2 times. The answer is in order of the first appearance in text.   

Function Description Complete the function stop_words in the editor below.   
* stop_words has the following parameter(s):     
* string text: the input text.     
* int k: the threshold occurrence count for a word to be a stop word   


**Returns**      
string[]: the list of stop words in order of their first occurrence 

***Constraints***: text has at most 50000 characters. Every character in text is either an English lowercase letter or a space. text starts and ends with a letter. No two consecutive characters are spaces, i.e. text is a valid sentence. There will be at least one stop word in the text. 1 ≤ k ≤ 18


------------------------------------------------------------------------------------------------------------------------------------------------------------------


7. We have a dataset about log of api request have name is `api_request_log`, include 3 columns:
* **id:** Represents the unique identifier of the account associated with the api request.
* **time:** Indicates the timestamp or date and time when the activity occurred. It is in the format 'MM:SS'.
* **status:** Status when user call a api, with 2 values, yes is call api sucessfull, no is call api failed.

Find time range a user call api failed between 2 times call api sucessfull (have type = yes), and count number of failed request. 

**Sample dataset:**

|id|time |type |
|---|---|-----------------------------|
1|0:23|yes
1|0:24|no
1|0:25|no
1|1:25|yes
1|1:26|no
1|2:26|no
1|3:36|no
1|4:26|no
2|10:26|yes
2|11:26|yes
2|12:26|no
2|13:27|no
2|16:27|yes

**After performing the steps:**

|id|type|from|to|activities|
|----------|-------|-----|-------|---|
|1       |no|0:24      |0:25   |2      |
|1     |no    |1:26   |4:26     |4
|2      |no|12:26     |13:27    |2     |
