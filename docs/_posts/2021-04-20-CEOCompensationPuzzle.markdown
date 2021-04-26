---
layout: post
title: CEO Compensation Puzzle
permalink: /CEO Compensation Puzzle
---

# The Question

    TEST YOUR INTUITION! Imagine ALL the workers in the USA (~200,000,000) worked for one company in a single hierarchy. At the bottom are minimum wage workers earning `$`10/hr. Every 5 minimum wage workers have a superior; every five superiors have their own superior and so on up the hierarchy to the Big Boss CEO (tree of degree 5). Every superior earns 1.3 times the wage of their subordinates i.e. `$`10 -> `$`13 -> `$`16.9 ... QUESTION: what is the hourly and annual wage of the Big Boss CEO??"

* Lets call the earnings multiplier `1.3` above the 'management multiplier'
* Lets call the number of workers per supervisor the 'team size'
* see below for a diagram of an example hierarchy where team size is 3 and the population of workers is 13

The mathematics of the model outlined above model is not very complicated but I suspect that intuition for what the Big Boss CEO should earn given such simple rules is not good - mine wasn't. This is likely because although the salary does grow exponentially up the hierarchy (like compound interest), the width of the hierarchy shrinks even faster. Below are presented some examples and interactive charts to explore the relationship between the size of teams, 'manager multiplier' and boss multiplier.

(An iteractive version of this notebook is published at the time of writing to [http://afternoon-oasis-29162.heroku.com] and the code is published to [https://github.com/hugoleeney/jupyter_notebooks/blob/main/Other/Fair%20Compensation.ipynb]




    
![svg](CEO%20Compensation%20Puzzle_files/CEO%20Compensation%20Puzzle_2_0.svg)
    







# Examples

In Ireland the number of workers is about 2,504,000.

The number of management levels in a hierarchy containing all 2,504,000 workers where each team 
has 5 employees would be 10.

If every level is paid 1.3 times the salary of the workers at the next level down 
then relative to the lowest level the maximum salary would be 14 times greater.

The minimum wage is 10.20 Euros, therefore the max hourly wage for a CEO would be 140.62 and the 
max annual salary for 40 hours a week would be 40 x 52 x max_hourly = 292,481 (discounting that
most CEOs would work more hours than this).

Below the calculation is repeated for worker population sizes roughly equivalent to the USA, China 
and Disney corporation.


|  | Ireland | US | China | Disney | Disney for `$`65M |
| --- | --- | --- | --- | --- | --- |
| # workers                           | 2,504,000 |200,000,000 |1,000,000,000 |200,000 | 200,000 | 
| # management levels with teams of 5 | 10 | 12       | 13       | 8 |8 |
| minimum wage                        | `$`10.2               | `$`10.2 | `$`10.2| `$`10.2|`$`10.2|
| boss multiplier                        | `$`1.3               | `$`1.3 | `$`1.3| `$`1.3|`$`2.72|
| Boss hourly wage                    | `$`141            | `$`238 | `$`309 | `$`83 |`$`30,560 |
| Boss annual salary (40 hrs a week)  | `$`292,481            | `$`494,292 | `$`642,580 | `$`173,065 | `$`63,564,515 |


Compare those outcomes with real-world Disney [2] where CEO Bob Iger’s 2019 compensation was `$` 65.6 Million in a 
company of 200,000 and a minimum wage of less than `$` 11. Iger's hourly rate for a 40hr week was equivalent
to about '$'30,000!

The final column of the table above includes details of a scenario where we set the manager multiplier for Disney
 so that the in our calculation the CEO salary is approximately correct. The required
multiplier for being a manager would be around 2.72. That means that if you were a manager of a 
concession stand or shop with a staff of 5 (those staff on the minimum wage of `$`10.2.) you would earn 
27.74 an hour or 57,708 a year. Their boss in turn would 
earn 156,964

Below in the interactive charts you can set a value for team size and/or manager multiplier and see what
the boss of such a scenario would earn under the stated rules.





# Effect of Team Size

Below you can see several charts of how the Boss Salary changes with the multiplier. Each chart has the team size set at a different value. Of course the smaller the team size the more management levels there are and the higher the Big Bosses salary. The value of the population used is 1,000,000.

This chart is available in interactive form at the link above.

![png]({{ site.baseurl }}/CEO%20Compensation%20Puzzle_files/CEO%20Compensation%20Puzzle_6_0.png){: .center-image }

# Effect of the Multiplier

Below you can see several charts of how the Boss Salary changes with the team-size. Each chart has the multipler set at a different value. Of course the higher the multiplier the larger the salary increase at each level. The value of the population used is 1,000,000.

This chart is available in interactive form at the link above.

![png]({{ site.baseurl }}/CEO%20Compensation%20Puzzle_files/CEO%20Compensation%20Puzzle_8_0.png){: .center-image }

# Tabulating Boss Salaries

Below find several tables that lists boss salaries by 
- team size (3 to 9) in the rows
- 'boss multiplier' (how much more a boss earns that their subordinates - 1.1 to 1.9) in the columns

Each table has a successively higher minimum wage. The value of the population used is 1,000,000.

This chart is available in interactive form where you can dynamically change the minimum wage and population at the link above. 

    Minimum Wage = 5



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1.1</th>
      <th>1.2</th>
      <th>1.3</th>
      <th>1.4</th>
      <th>1.5</th>
      <th>1.6</th>
      <th>1.7</th>
      <th>1.8</th>
      <th>1.9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>$35,904</td>
      <td>$111,273</td>
      <td>$314,990</td>
      <td>$825,463</td>
      <td>$2,024,043</td>
      <td>$4,683,744</td>
      <td>$10,300,761</td>
      <td>$21,655,883</td>
      <td>$43,735,103</td>
    </tr>
    <tr>
      <th>4</th>
      <td>$26,975</td>
      <td>$64,394</td>
      <td>$143,373</td>
      <td>$300,825</td>
      <td>$599,716</td>
      <td>$1,143,492</td>
      <td>$2,096,634</td>
      <td>$3,713,286</td>
      <td>$6,376,309</td>
    </tr>
    <tr>
      <th>5</th>
      <td>$24,523</td>
      <td>$53,662</td>
      <td>$110,287</td>
      <td>$214,875</td>
      <td>$399,811</td>
      <td>$714,683</td>
      <td>$1,233,314</td>
      <td>$2,062,937</td>
      <td>$3,355,952</td>
    </tr>
    <tr>
      <th>6</th>
      <td>$22,293</td>
      <td>$44,718</td>
      <td>$84,836</td>
      <td>$153,482</td>
      <td>$266,541</td>
      <td>$446,677</td>
      <td>$725,479</td>
      <td>$1,146,076</td>
      <td>$1,766,291</td>
    </tr>
    <tr>
      <th>7</th>
      <td>$22,293</td>
      <td>$44,718</td>
      <td>$84,836</td>
      <td>$153,482</td>
      <td>$266,541</td>
      <td>$446,677</td>
      <td>$725,479</td>
      <td>$1,146,076</td>
      <td>$1,766,291</td>
    </tr>
    <tr>
      <th>8</th>
      <td>$20,267</td>
      <td>$37,265</td>
      <td>$65,258</td>
      <td>$109,630</td>
      <td>$177,694</td>
      <td>$279,173</td>
      <td>$426,752</td>
      <td>$636,709</td>
      <td>$929,627</td>
    </tr>
    <tr>
      <th>9</th>
      <td>$20,267</td>
      <td>$37,265</td>
      <td>$65,258</td>
      <td>$109,630</td>
      <td>$177,694</td>
      <td>$279,173</td>
      <td>$426,752</td>
      <td>$636,709</td>
      <td>$929,627</td>
    </tr>
  </tbody>
</table>
</div>


    Minimum Wage = 10



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1.1</th>
      <th>1.2</th>
      <th>1.3</th>
      <th>1.4</th>
      <th>1.5</th>
      <th>1.6</th>
      <th>1.7</th>
      <th>1.8</th>
      <th>1.9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>$71,807</td>
      <td>$222,546</td>
      <td>$629,980</td>
      <td>$1,650,927</td>
      <td>$4,048,086</td>
      <td>$9,367,487</td>
      <td>$20,601,522</td>
      <td>$43,311,767</td>
      <td>$87,470,206</td>
    </tr>
    <tr>
      <th>4</th>
      <td>$53,950</td>
      <td>$128,788</td>
      <td>$286,746</td>
      <td>$601,650</td>
      <td>$1,199,433</td>
      <td>$2,286,984</td>
      <td>$4,193,267</td>
      <td>$7,426,572</td>
      <td>$12,752,618</td>
    </tr>
    <tr>
      <th>5</th>
      <td>$49,045</td>
      <td>$107,323</td>
      <td>$220,574</td>
      <td>$429,750</td>
      <td>$799,622</td>
      <td>$1,429,365</td>
      <td>$2,466,628</td>
      <td>$4,125,873</td>
      <td>$6,711,904</td>
    </tr>
    <tr>
      <th>6</th>
      <td>$44,587</td>
      <td>$89,436</td>
      <td>$169,672</td>
      <td>$306,964</td>
      <td>$533,081</td>
      <td>$893,353</td>
      <td>$1,450,958</td>
      <td>$2,292,152</td>
      <td>$3,532,581</td>
    </tr>
    <tr>
      <th>7</th>
      <td>$44,587</td>
      <td>$89,436</td>
      <td>$169,672</td>
      <td>$306,964</td>
      <td>$533,081</td>
      <td>$893,353</td>
      <td>$1,450,958</td>
      <td>$2,292,152</td>
      <td>$3,532,581</td>
    </tr>
    <tr>
      <th>8</th>
      <td>$40,533</td>
      <td>$74,530</td>
      <td>$130,517</td>
      <td>$219,260</td>
      <td>$355,388</td>
      <td>$558,346</td>
      <td>$853,504</td>
      <td>$1,273,418</td>
      <td>$1,859,253</td>
    </tr>
    <tr>
      <th>9</th>
      <td>$40,533</td>
      <td>$74,530</td>
      <td>$130,517</td>
      <td>$219,260</td>
      <td>$355,388</td>
      <td>$558,346</td>
      <td>$853,504</td>
      <td>$1,273,418</td>
      <td>$1,859,253</td>
    </tr>
  </tbody>
</table>
</div>


    Minimum Wage = 15



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1.1</th>
      <th>1.2</th>
      <th>1.3</th>
      <th>1.4</th>
      <th>1.5</th>
      <th>1.6</th>
      <th>1.7</th>
      <th>1.8</th>
      <th>1.9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>$107,711</td>
      <td>$333,819</td>
      <td>$944,970</td>
      <td>$2,476,390</td>
      <td>$6,072,129</td>
      <td>$14,051,231</td>
      <td>$30,902,283</td>
      <td>$64,967,650</td>
      <td>$131,205,308</td>
    </tr>
    <tr>
      <th>4</th>
      <td>$80,925</td>
      <td>$193,182</td>
      <td>$430,118</td>
      <td>$902,475</td>
      <td>$1,799,149</td>
      <td>$3,430,476</td>
      <td>$6,289,901</td>
      <td>$11,139,858</td>
      <td>$19,128,927</td>
    </tr>
    <tr>
      <th>5</th>
      <td>$73,568</td>
      <td>$160,985</td>
      <td>$330,860</td>
      <td>$644,625</td>
      <td>$1,199,433</td>
      <td>$2,144,048</td>
      <td>$3,699,942</td>
      <td>$6,188,810</td>
      <td>$10,067,856</td>
    </tr>
    <tr>
      <th>6</th>
      <td>$66,880</td>
      <td>$134,154</td>
      <td>$254,508</td>
      <td>$460,446</td>
      <td>$799,622</td>
      <td>$1,340,030</td>
      <td>$2,176,436</td>
      <td>$3,438,228</td>
      <td>$5,298,872</td>
    </tr>
    <tr>
      <th>7</th>
      <td>$66,880</td>
      <td>$134,154</td>
      <td>$254,508</td>
      <td>$460,446</td>
      <td>$799,622</td>
      <td>$1,340,030</td>
      <td>$2,176,436</td>
      <td>$3,438,228</td>
      <td>$5,298,872</td>
    </tr>
    <tr>
      <th>8</th>
      <td>$60,800</td>
      <td>$111,795</td>
      <td>$195,775</td>
      <td>$328,890</td>
      <td>$533,081</td>
      <td>$837,519</td>
      <td>$1,280,257</td>
      <td>$1,910,126</td>
      <td>$2,788,880</td>
    </tr>
    <tr>
      <th>9</th>
      <td>$60,800</td>
      <td>$111,795</td>
      <td>$195,775</td>
      <td>$328,890</td>
      <td>$533,081</td>
      <td>$837,519</td>
      <td>$1,280,257</td>
      <td>$1,910,126</td>
      <td>$2,788,880</td>
    </tr>
  </tbody>
</table>
</div>


    Minimum Wage = 20



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1.1</th>
      <th>1.2</th>
      <th>1.3</th>
      <th>1.4</th>
      <th>1.5</th>
      <th>1.6</th>
      <th>1.7</th>
      <th>1.8</th>
      <th>1.9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>$143,614</td>
      <td>$445,092</td>
      <td>$1,259,960</td>
      <td>$3,301,853</td>
      <td>$8,096,171</td>
      <td>$18,734,974</td>
      <td>$41,203,045</td>
      <td>$86,623,534</td>
      <td>$174,940,411</td>
    </tr>
    <tr>
      <th>4</th>
      <td>$107,900</td>
      <td>$257,576</td>
      <td>$573,491</td>
      <td>$1,203,299</td>
      <td>$2,398,866</td>
      <td>$4,573,968</td>
      <td>$8,386,535</td>
      <td>$14,853,144</td>
      <td>$25,505,236</td>
    </tr>
    <tr>
      <th>5</th>
      <td>$98,091</td>
      <td>$214,647</td>
      <td>$441,147</td>
      <td>$859,500</td>
      <td>$1,599,244</td>
      <td>$2,858,730</td>
      <td>$4,933,256</td>
      <td>$8,251,746</td>
      <td>$13,423,808</td>
    </tr>
    <tr>
      <th>6</th>
      <td>$89,173</td>
      <td>$178,872</td>
      <td>$339,344</td>
      <td>$613,928</td>
      <td>$1,066,162</td>
      <td>$1,786,706</td>
      <td>$2,901,915</td>
      <td>$4,584,304</td>
      <td>$7,065,162</td>
    </tr>
    <tr>
      <th>7</th>
      <td>$89,173</td>
      <td>$178,872</td>
      <td>$339,344</td>
      <td>$613,928</td>
      <td>$1,066,162</td>
      <td>$1,786,706</td>
      <td>$2,901,915</td>
      <td>$4,584,304</td>
      <td>$7,065,162</td>
    </tr>
    <tr>
      <th>8</th>
      <td>$81,067</td>
      <td>$149,060</td>
      <td>$261,034</td>
      <td>$438,520</td>
      <td>$710,775</td>
      <td>$1,116,691</td>
      <td>$1,707,009</td>
      <td>$2,546,835</td>
      <td>$3,718,506</td>
    </tr>
    <tr>
      <th>9</th>
      <td>$81,067</td>
      <td>$149,060</td>
      <td>$261,034</td>
      <td>$438,520</td>
      <td>$710,775</td>
      <td>$1,116,691</td>
      <td>$1,707,009</td>
      <td>$2,546,835</td>
      <td>$3,718,506</td>
    </tr>
  </tbody>
</table>
</div>






# Differences to Real World


Obviously the stated rules are not how things work in the real world. They vastly under-predict the amount
that companies/share-holders see fit to pay their CEOs. Also of course no country or company has a 
single hierarchy. Countries have many companies and organisiations. Companies themselves have departments, 
branches, business units etc. You might think that this would cause the above model to over-predict - after all
this means that the average hierarchy will be shallower. However
competition for talent between industries and companies could also drive salaries up and at the end of
the day companies pay what they can afford which has more to do with the specific industry, profitability and
investor mindsets.

Here are some more reasons why the model might underpredict salaries.


* specialities/more valuable or rare skills - supply and demand
* years of education 
    - acts as an investment, must be repaid
    - adds to possible value, rarity
* jobs no-one wants to do / hours that they don't want to work
* incentivise the 'best' people to do the most important work
* incentivise people to not misbehave in positions of asymmetric power (although questionable if this would ever work)
* ...

Of course we must also recognize that a CEO doesn't necessarily get compensated in cash like a regular employee 
does and so comparing the two `$` value compensations can be problematic.


# Power Dynamics & (possibly) a Better (but still simple) Model

One other key factor in the disparity between the model and the real world could be that as employees 
rise in an organisation they have more influence over how much they get paid. Lets try to model that 
phenomenon.

In the model used above the sequence of wages at each level forms a geometric sequence (the next number in the
sequence is some multiple of the previous number). Lets keep the simple hierarchy but say that at each 
managerial level the employee earns a higher multiple of their subordinates salary. 

For example, lets try to increase the management multiplier by a fixed value 0.3 at each level. This means 
that we now have an arithmetic sequence (grows by a fixed amount) for the multiplier. 
The first 3 multiplier values will be 1.3, 1.6, 1.9 ... We will use 8 levels of management as there would be
in the case of Disney. At the 8th the CEO will earn 3.4 times his direct reports. 

- bottom level: `$`10
- level 1: (x 1.3) `$` 13.00
- level 2: (x 1.6) `$` 20.80 
- level 3: (x 1.9) `$` 39.52
- level 4: (x 2.2) `$` 86.94
- level 5: (x 2.5) `$` 217.36
- level 6: (x 2.8) `$` 608.61
- level 7: (x 3.1) `$` 1,886.68
- level 8: (x 3.4) `$` 6,414.73

This model produces a CEO hourly rate of `$` 6,414.73 whereas in Disney's case
it was closer to `$`30k (based on a 40hr week). 

To produce a 30k figure we'd have to start at 1.3 for the first level of management and increase the
management multiplier by about 0.47 at each level. 

- bottom level: `$`10
- level 1: (x 1.3) `$` 13.0
- level 2: (x 1.77) `$` 23.01
- level 3: (x 2.24) `$` 51.54
- level 4: (x 2.71) `$` 139.68
- level 5: (x 3.18) `$` 444.18
- level 6: (x 3.65) `$` 1,621.26
- level 7: (x 4.12) `$` 6,679.61
- level 8: (x 4.59) `$` 30,659.41

This is still somewhat unsatisfactory. The arithmetic increase in management multiplier means that the first 
3 levels of employee earn 10, 13 and 23 dollars respectively. This seems to be too fast an increase.

We could try a geometric increase in the multiplier i.e. the multiplier would grow by some multiple at each
level instead of by a fixed value. Below we will start with a smaller multiplier of 1.2 but we will grow the
multiplier by 1.323 at i.e. 1.2 -> 1.59 -> 2.10 ...

- bottom level: `$`10
- level 1: (x 1.2) `$` 12.0
- level 2: (x 1.59) `$` 15.88
- level 3: (x 2.10) `$` 27.79
- level 4: (x 2.78) `$` 64.35
- level 5: (x 3.68) `$` 197.14
- level 6: (x 4.86) `$` 799.06
- level 7: (x 6.43) `$` 4,284.87
- level 8: (x 8.51) `$` 30,398.83

That has flattened out the bottom end and feels a little bit more realistic. However note that the CEOs
direct reports are all still making nearly 9 million a year. Whether or not that is accurate I don't know.
If we had details of all Disney employees' salaries we would be able to do a much more in depth modelling
exersize - perhaps some kind of regression. That's beyone the scope of this short article though. Disney 
probably has far more than 8 seniority levels across the company. It also has many business units and 
functional departments that make a single-hierarchy model only so useful. What we can conclude is that to 
get from a low hourly wage of `$`10 to an annual salary of `$`65 million means making very big jumps between
levels of seniority - jumps that can't be accounted for by a simple compounding rate of increase. Such a 
disparity in income would be outrageous in the civil service, army and other 
public sector organisations. We should probably expect a different dynamic in the private sector but 
discomprehension and outrage at compensation such as Bob Iger's in the year stated above is understandable.



## Public Sector


There are many examples of where this model doesn't work in the private sector. It vastly 
under-predicts the amount that companies/share-holders see fit to pay their CEOs. There are two public 
sector examples I want to draw attention to. 

The first is the salary of the President of the USA - `$`400,000 a year. The second is the 
Prime Minister of Ireland - about €210,000. Those aren't that far off the numbers generated in the 
exammples above and that is
curious. Of course the head of state doesn't sit on top of a single hierarchy of workers but rather 
(in a democracy) should be a specialist from a relatively small pool of candidates. 

Many public pay structures are in/reviewed in the public domain [4].





# Conclusion

What MIGHT seem like a fair way to decide how much people at higher and higher levels of responsibility in an organisation should earn does not predict well what upper levels of management earn in firms around the world. It does seem that the increases employees see as they 'climb the ladder' in the private sector are probably somewhat geometric in nature. 

### References

[1] About wealth inequality ... https://www.theguardian.com/commentisfree/2018/apr/12/wealth-inequality-reasons-richest-global-gap]

[2] Figures for Disney ... https://www.forbes.com/sites/markmurphy/2019/04/23/abigail-disney-is-right-insane-ceo-compensation-can-have-a-corrosive-effect-on-society/

[3] Example of more in depth research in this topic ... https://www.sciencedirect.com/science/article/abs/pii/S0378426613001234

[4] https://www.ipa.ie/_fileUpload/Documents/CPMR_DP_38_Review_ofthe_Civil_Service_Grading_Pay_System.pdf
