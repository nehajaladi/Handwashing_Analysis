# Handwashing_Analysis
Analyzing the data to determine whether handwashing had any impact on the deaths of women giving birth during the early 1840s at the Vienna General Hospital.

## Dr. Semmelweis
In the 19th century, before the discovery of bacteria, it was not well understood how diseases spread. Dr. Semmelweis observed that the mortality rate at Clininc 2 where midwives worked was much higher than at the Clinic 1 where medical students worked. He hypothesized that medical students, who also performed autopsies, may have been unknowingly transmitting infection to the women they were treating in the maternity ward.

To test his hypothesis, Dr. Semmelweis implemented a strict hand-washing protocol for medical students and other staff who worked in the maternity ward.

## Project Outline
In this project we will look analyse a few things in this order.

### 1.Reading the dataset
The table below shows the number of women giving birth at the two clinics (clinic 1 & clinic 2) between the years 1841 to 1846 at the Vienna General Hospital.

![image](https://user-images.githubusercontent.com/38401969/219965655-670d569f-bb37-4ffb-90f6-aa379b768f8f.png)


### 2.Checking the Mortality rates
From the above table we can see that many women died while giving birth. To analyze the proportion of deaths at Clinic 1 & 2, we need to look at the number of deaths in relation to the total number of women who gave birth at the clinic. If we divide the number of deaths by the total number of births and then multiply by 100, we can calculate the percentage of deaths. For example, if there were 100 births and 5 deaths, the proportion of deaths would be 5%.

![image](https://user-images.githubusercontent.com/38401969/219965858-46c75ef9-d7d5-4aa8-bccf-f35f5300173f.png)

### 3.Visualizing the Mortality rates
If we plot the proportion of deaths on a graph, we can see an interesting pattern.

![image](https://user-images.githubusercontent.com/38401969/219965901-c1a82d35-1097-460c-bb58-e50985ce31fc.png)

### 4.Handwashing protocol
There seems to be clearly a difference in the mortality rates between Clinic 1 and Clinic 2. Proportion of Deaths in Clinic 2 is much higher than Clinic two consistently for so many years.We will be analysing whether the hand-washing protocol had any significant impact on the mortality rates. For this, we will be looking at another dataset with monthly data of births and deaths.

![image](https://user-images.githubusercontent.com/38401969/219966120-f1ff9cf1-fb84-4ab5-a942-0350f055fdf8.png)

### 5.The effect of handwashing

Plotting the data of the monthly_data dataframe will help us understand how the proportion of deaths changed overtime. Inorder to highlight the difference before and after started the handwashing protcol,we will be using different colors in the plot.

![image](https://user-images.githubusercontent.com/38401969/219966087-ab6a3561-9b84-4cab-b719-e1146859452b.png)

### 6.Highlighting the effect of handwashing

From the above graph, we can see that from mid of 1847 the proportions of deaths have been drastically reduced. That also happens to the time period when Dr.Semmelweis had made the handwashing mandatory.

![image](https://user-images.githubusercontent.com/38401969/219966165-3dd6f77d-9bfc-49ae-ad49-1de3019ac81b.png)

### 7.More handwashing = fewer deaths?

How much did it reduce the monthly proportion of deaths on average? Lets calculate the difference in means between the proportion of deaths before and after handwashing was introduced.

![image](https://user-images.githubusercontent.com/38401969/219966237-917d1586-2a99-41ae-afb6-8bf23944ca88.png)

### 8.Performing a Bootstrap analysis.

We can see that implementing the handwashing protocol reduced the proportion of deaths by around 8% points. This mean its reducted on an average from 10% to 2%.

If the difference in mortality rates between Clinic 1 and Clinic 2 is due to differences in hygiene practices, then it may be possible to improve outcomes by implementing better infection control measures in Clinic 2.

Lets look at the confidence interval to see the uncertainity around how much handwashing reduces mortality rates.

A confidence interval is a range of values that is likely to contain the true effect of an intervention (such as handwashing) with a certain degree of confidence. The bootstrap method is a statistical technique for estimating the variability of an estimate by resampling the data.

![image](https://user-images.githubusercontent.com/38401969/219966280-142949c9-a0fc-4d45-ac29-2facb50946ef.png)

### 9.Conclusion

So handwashing reduced the proportion of deaths by between 6.7 and 10 percentage points, according to a 95% confidence interval. This provided strong evidence that handwashing was a simple yet highly effective procedure that could save many lives.

