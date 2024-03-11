<h1 align="center">Data analysis</h1>

![analiseimagem](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/9b0fc301-509f-4766-8617-003f05568385)

<h3>Case: Customer Cancellation</h3>

<p>A large company recently realized that of its total customer base, the majority are inactive customers, that is, those who have already canceled the service.</p>
<p>Needing to improve its results, the company wants to understand the reasons that led to cancellation, and what are the most efficient actions to reduce this number.</p>

---

Tools Used:
- Python <img align="center" height="20" width="30" alt="js-icon"  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
- Pandas Library
- Jupyter Anaconda

---

<h1>Importing the Database</h1>

<p>I imported the library pandas, after importing the library I used 'pd.read_csv' to read our file which is in csv format. And assigning the table to a variable</p>

![1](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/a8c2c763-72ad-43ed-ba20-dd5f46944a80)

<h3>I used the display command to visualize our database.</h3>

![2](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/279c513a-e4a4-4139-a249-edf006794e53)


---


<h1>Removing Empty Data</h1>

<p>Before starting with the analysis it is essential carry out data processing, as well as avoids causing errors due to unnecessary data or even non-existent.</p>
<p> I used the command 'table.dropna' to remove the empty information from our table.</p>

![3](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/037ec4b6-409c-4382-b3fe-2e8817fd2eb9)


---


<h1>Data Analysis</h1>

<h3>Checking the Cancellation Rate</h3>

<p>I started by analyzing the company's cancellation rate, because the objective is to reduce it. So we'll have to check what this rate is and find out where it comes from.</p>

<p>I used the 'tabela[“cancelou”].value_counts' to check the amount of information we have in the “cancelled” column of the table.</p>

<p>This way we will be able to visualize with the display which is the proportion of customers who canceled and who continue with the signature.</p>

![5](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/32c4ac22-efa8-4a9c-8a8e-6f4701ca625f)

<p>The first view will show the data count, who canceled (1) and those who did not cancel (0).  In the second view, we will normalize and format in percentage, this makes it easier to analyze which proportion of customers who are canceling the service.</p>

<p>Note that we have a total of 56.7% cancellation of subscriptions, so more than half of customers are canceling the service.</p>

<p>So let's find out where this number comes from.</p>


---


<h1>Checking Contract Cancellation</h1>

<p>We have already seen how the customer cancellation relationship is, now We can take a look at the duration of these contracts customers.</p>

<p>Remembering that we have 3 types of contract: monthly, quarterly and Annual. So it's interesting to see what this proportion is like for check whether this could be a factor that directly affects the
cancellation of service.</p>

![6](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/f62a3cca-01ce-4a35-a429-f2c148ddd9f2)

With this simple analysis you can already see that we have the following proportion in the duration of contracts:
- Annual 40,19%
- Quarterly 40,00%
- Monthly 19,75%

<p>We have an almost equal division between the annual and quarterly, but the monthly plan is already behind with almost 20%.</p>

<p>I analyzed the contract information to check how they are distributed and check if any of them have a higher cancellation percentage.</p>


---

<h1>Analyzing Contract Information</h1>

<p>I used 'groupby' to group the information from the 'contract_duration' column and then average the information we have in the table.</p>

<p>This will give more general information about each one of these plans, and we can check if there is any important information.</p>

![7](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/4fd859c8-9322-4dab-8f4d-00da39b20b13)

<p>With the information grouped, it is possible to notice that the customers of the Monthly plan, have an average cancellation rate of 1, that is, practically all customers who use this plan canceled the service.</p>

<p>This is already an important point within our analysis, as there is a plan from this company, where practically all customers cancel the service</p>


---

<h1>Removing the Monthly Contract</h1>

<p>Knowing that the monthly contract is not a good option for the company, we can remove the information from this specific contract and continue analyzing.</p>

![8](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/465918a7-d2dd-47c8-a0f2-34abe87b8bba)

<p>Note that the proportion of cancellations have already fallen to 46.1% in this analysis, but this number is still very high.</p>

<p>So let's continue analyzing to arrive at an acceptable value of cancellations that are not close to 50%.</p>


---

<h1>Analyzing the Plan Subscriptions</h1>

<p>As we still have a very high number of cancellations, we will now make a analysis on signatures to see if we can draw any conclusions to improve this cancellation rate.</p>

<p>First, let's count the values ​​in the signatures column to find out how many subscriptions we have in each of the plans.</p>

<p>Next, we will group the information by signature and obtain the average of the lines for each of the columns.</p>

![9](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/73493d6e-d2ce-4018-b408-d0107d99d993)

<p>In the initial analysis, we can see that we have almost the same quantity in each of the subscriptions, that is, we have almost 1/3 in each subscription.</p>

<p>In the second analysis, we find that the cancellation values are also very similar.</p>

<p>We cannot exclude any information as the data is virtually identical. This means we will have to delve deeper into our data analysis.</p>

---

<h1>Graphical Analyses</h1>

<p>To create the graphs, we will use the 'plotly.express' library.</p>

![10 - criango graficos](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/1e373590-e48b-4e27-9d24-3ade114ac634)

<p>Now, I've used the For loop structure to iterate through each of the columns of our table. With this, we will create a histogram graph for each column, so we can analyze each piece of information and see how they relate to the company's cancellations.</p>


<p>In this graph, it's noticeable that customers with more than 20 days of overdue cancel their subscriptions.</p>

![dias_atraso](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/c448c461-48c1-4ae0-874a-5d17c900a8f6)
#

<p>In this other graph, it's noticeable that customers who make more than 5 phone calls to the call center tend to cancel their subscriptions.</p>

![call_center](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/c1c97f02-3874-4e75-8e16-3f2762f42dd9)
#

<p>Analyzing only the two indicated graphs, we can keep in the table the calls to the call center that are less than 5.</p>

<p>And we can also keep the information where the days overdue are less than 0.</p>

<p>With this, we can visualize the database and recalculate to verify the cancellation percentage. Note that by only removing the information from these two columns, we went from a cancellation rate of almost 50% to 18.4%. We had to go through several steps to reach an 'acceptable' value.</p>

![11](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/e4be7695-f419-4522-b70b-bffef907ed59)


![12](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/5eb87bad-2029-454b-8fbe-62a5a53ff528)

---

<h1>Conclusion</h1>

<p>We started the analysis with a cancellation rate of 56.7%. After the initial treatment, we managed to decrease it slightly to 46.1%.</p>

<p>In the end, with the help of the graphs, we managed to adjust our database and reached a cancellation rate of 18.4%.<p>

<p>And by conducting all these analyses and treatments, we can show the company where the issues lie and what can be done to minimize cancellations.</p>
