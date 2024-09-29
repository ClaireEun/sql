# Assignment 1: Design a Logical Model
Participaint name : Claire Eun

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
Type 1: Overwrite – In this approach, any changes to the address will overwrite the existing address, erasing the previous one. As a result, only the most recent address will be stored for each customer.

Type 2: Retain Changes – This approach retains a history of all address changes. Each time a new address is added, the previous address remains in the system. This method requires additional columns, such as start and end dates, to track when each address was valid.

Privacy implication : The type 2 could cause privacy issues because previous information could be misused. 

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Your answer...
1. Difference in Data Classification Due to Company Size : The AdventureWorks ERD seems to represent a much larger company compared to my book store. Since My bookstore is small, so there are no need to have tabels like manufacturing, human resources, or purchasing. However, I think it could be a good idea to add simplified Purchasing table in the future. Even small bookstores need to track book purchases, and having that data stroed could be beneficial for the future.

2. Level of Detail in Data Tables: AdventureWorks features highly detailed tables for sales, such as separate tables for SalesOrderHeader, SalesOrderDetail, and TransactionHistory. This allows them to manage complex data and large volumes efficiently. My bookstore ERD, on the other hand, is simpler and consists of a single Sales table. While I don’t require that level of detail at this time, I recognize that adding separate tables for Tax and Payment Methods (like credit cards) could enhance data management and provide more detailed reporting on sales in the future.

Yes I would like to adding Purchasing table and breaking down the Sales table further.

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
