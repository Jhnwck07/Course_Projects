select count(id) as Total_Loan_Applications from bank_loan_data
select count(id) as MTD_Loan_Applications from bank_loan_data
where month(issue_date) = 12 and year(issue_date) = 2021
select count(id) as PMTD_Loan_Applications from bank_loan_data
where month(issue_date) = 11 and year(issue_date) = 2021


select sum(loan_amount) as Total_Funded_Amount from bank_loan_data
select sum(loan_amount) as MTD_Total_Funded_Amount from bank_loan_data
where month(issue_date) = 12 and year(issue_date) = 2021
select sum(loan_amount) as PMTD_Total_Funded_Amount from bank_loan_data
where month(issue_date) = 11 and year(issue_date) = 2021


select sum(TOTAL_PAYMENT) as Total_Amount_Received from bank_loan_data
select sum(TOTAL_PAYMENT) as MTD_Total_Amount_Received from bank_loan_data
where month(issue_date) = 12 and year(issue_date) = 2021
select sum(TOTAL_PAYMENT) as PMTD_Total_Amount_Received from bank_loan_data
where month(issue_date) = 11 and year(issue_date) = 2021


select round(avg(int_rate),4)*100 as Avg_Int_Rate from bank_loan_data
select round(avg(int_rate),4)*100 as MTD_Avg_Int_Rate from bank_loan_data
where month(issue_date) = 12 and year(issue_date) = 2021
select round(avg(int_rate),4)*100 as PMTD_Avg_Int_Rate from bank_loan_data
where month(issue_date) = 11 and year(issue_date) = 2021


select round(avg(dti),4)*100 as Avg_DTI from bank_loan_data
select round(avg(dti),4)*100 as Avg_DTI from bank_loan_data
where month(issue_date) = 12 and year(issue_date) = 2021
select round(avg(dti),4)*100 as Avg_DTI from bank_loan_data
where month(issue_date) = 11 and year(issue_date) = 2021



select(count(case when loan_status = 'Fully Paid' OR loan_status = 'Current' then id end) * 100.0) / count(id) as Good_Loan_Percentage
from bank_loan_data

select count(id) as Good_loan_Applications from bank_loan_data 
where loan_status = 'Fully Paid' or loan_status = 'Current' 

select sum(loan_amount) as Good_Loan_Funded_Amount from bank_loan_data
where loan_status = 'fully paid' or loan_status = 'current'

select sum(total_payment) as Good_Loan_Total_Received_Amount from bank_loan_data
where loan_status = 'fully paid' or loan_status = 'current'



select(count(case when loan_status = 'charged off' then id end) * 100.0) / count(id) as Bad_Loan_Percentage
from bank_loan_data

select count(id) as Bad_loan_Applications from bank_loan_data 
where loan_status = 'charged off' 

select sum(loan_amount) as Bad_Loan_Funded_Amount from bank_loan_data
where loan_status = 'charged off'

select sum(total_payment) as Bad_Loan_Total_Received_Amount from bank_loan_data
where loan_status = 'charged off'



select 
		loan_status, 
		count(id) as Loan_Count, 
		sum(total_payment) as Total_Amount_Received,
		sum(loan_amount) as Total_Funded_Amount,
		avg(int_rate*100) as Int_Rate,
		avg(dti) as DTI
from bank_loan_data
group by loan_status


select 
		loan_status,
		sum(total_payment) as MTD_Total_Amount_Received,
		sum(loan_amount) as MTD_total_Funded_Amount
from bank_loan_data
where month(issue_date) = 12
group by loan_status



select
	month(issue_date) as Month_Munber, 
	datename(month, issue_date) as Month_name, 
	count(id) as Total_Loan_Applications,
	sum(loan_amount) as Total_Funded_Amount,
	sum(total_payment) as Total_Amount_Received
from bank_loan_data
group by month(issue_date), datename(month, issue_date)
order by month(issue_date)


select 
		address_state as State,
		count(id) as Total_no_of_Applications,
		sum(loan_amount) as Total_Funded_Amount,
		sum(total_payment) as Total_Received_amount
from bank_loan_data
group by address_state
order by count(id) desc


select 
		term as Term,
		count(id) as Total_no_of_Applications,
		sum(loan_amount) as Total_Funded_Amount,
		sum(total_payment) as Total_Received_amount
from bank_loan_data
group by term
order by term


select
	emp_length as Employee_Length, 
	count(id) as Total_Loan_Applications,
	sum(loan_amount) as Total_Funded_Amount,
	sum(total_payment) as Total_Amount_Received
from bank_loan_data
group by emp_length
order by emp_length


select
	purpose as PURPOSE, 
	count(id) as Total_Loan_Applications,
	sum(loan_amount) as Total_Funded_Amount,
	sum(total_payment) as Total_Amount_Received
from bank_loan_data
group by purpose
order by purpose


select 
	home_ownership as Home_Ownership, 
	count(id) as Total_Loan_Applications,
	sum(loan_amount) as Total_Funded_Amount,
	sum(total_payment) as Total_Amount_Received
from bank_loan_data
group by home_ownership
order by home_ownership










