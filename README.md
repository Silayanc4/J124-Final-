# J124 Final on Juvenile Court Schools and Free and Reduced Priced Meals Database 
by Silayan Camson

1. Story & Sourcing 
2. Data Analysis 
3. Data Visualization 

## Story Pitch

Students who are Free and Reduced Price Meal Eligible are described in the data set as
“(1) applying for the National School Lunch Program (NSLP); (2) submitting alternative household income forms; (3) student homeless, migrant, or tribal foster youth statuses in CALPADS;  (4) being "directly certified" through CALPADS as participating in California's food stamp or CalWORKs programs or (5) being identified through the weekly CALPADS Foster Matching process or matched by the LEA through the CALPADS online match process as being in Foster Placement, Foster Family Maintenance, or Tribal Foster on Census day”.

I wanted to observe FRPM data within Juvenile Court Schools, but soon saw that 100% of the students within Juvenile Court Schools were FRPM eligible. I wanted to specifically focus on where Juvenile Court Schools were concentrated. Comparing Juvenile Court Schools within their own county by FRPM levels also helped put their FRPM into a local context. Larger differences between the FRPM levels of Juvenile Court Schools and the rest of their county might be concerning and worth exploring on even smaller scales like cities. Higher counts of Juvenile Court Schools could also be worth exploring for negligence or high socioeconomic difference within the county- especially with larger differences in FRPM eligibility in a local context. 

## Additional Sourcing 
### ![School Accountability Report Card](https://www.sarconline.org/public/findASarc) 
Each school would show a lot more data on demographics, English learning percentages, and homelessness. 

### Department of Justice (2020). Criminal Justice Data. Juvenile Court and Probation.
The department of justice’s [website](https://data-openjustice.doj.ca.gov/sites/default/files/2021-06/Juvenile%20Justice%20In%20CA%202020.pdf) is not working, so data must be requested in order to get access to it. This would show sentencing data and if they are possibly getting transferred to an adult facility. 

## Sources 
### Tapau Osborne
Senior Program Specialist 

Juvenile Court Schools 

(562)-922-6343
osborne_tapau@lacoe.edu 

LA county of Education 

Osborne is a Senior Program Specialist within the county that has the most Juvenile Court Schools 

### Katy Foster
Principal 

1111 Las Gallinas Avenue
PO Box 4935
San Rafael, CA 94913

(415)-491-0581

kfoster@marinschools.org

Marin County Office of Education

This is displayed on the school's website currently 
>*Should you wish to receive a printed copy of the School Accountability Report Card for this program, please contact
Education Services: 415-499-5870 or ltrahan@marinschools.org

Foster is the principal of Loma Alto Juvenile Court School in Marin County, which is the county with the second highest disparity between the Juvenile Court School and the other schools for eligibility percentage for FRMP.

### Marcus Jarvin 
Outreach and Communications Associate, Debt Free Justice Campaign

![Juvenile Law Center](https://jlc.org/children-prison) 

Media and Press Inquiries: press@jlc.org

Local: (215) 625-0551

Jarvin has over 10 years of experience working with juvenile justice reform, with a special focus on education and juvenile sentence expungement. Jarvin also went through the juvenile court education system. 

# Data Analysis 
### Here are my guiding questions 
1. How many juvenile court schools are there and where are they?
2. How populated are they? 
3. What is the free and reduced lunch average for these juvenile court schools? 
4. How do these juvenile court schools compare to other types of schools for eligible Free Lunches?
5. Which counties have the biggest difference between the percentage of free and reduced lunch eligible students of their juvenile court schools and the rest of the schools? 

## Download this [dataset](https://www.cde.ca.gov/ds/ad/filessp.asp) as a CSV file 
## Here is *[my dataset](https://docs.google.com/spreadsheets/d/1WL1D8wbMM-r2la69j0H0akfdj5uftsPqEpW92ik-GIs/edit?usp=sharing)* that I used 

## How many juvenile court schools are there and where are they?
1. Isolate the juvenile court schools by filtering them 
![filtering juvenile schools](https://user-images.githubusercontent.com/109619685/183434382-596680d4-bce8-443c-9a81-2ee5f125725f.png)
2. Copy and Paste them into a Pivot Table 
3. Make the rows their "County Names" and "County Codes" and the Value as "School Type" 
4. Name this "Location and Count"
[location and count](https://user-images.githubusercontent.com/109619685/183460804-c30b7922-67c6-4567-bd3d-160b639d2b2e.png)

## How populated are they? 
1. Add to "Location and Count" the value of "SUM of Free Meal Count" 
[meal count](https://user-images.githubusercontent.com/109619685/183436086-5fbd23a0-47f6-4ad4-9170-d7ce517ee658.png) 
the most populated juvenile court schools are Los Angeles, Orange, San Diego, and Kern Counties
[most populated juvenile court schools](https://user-images.githubusercontent.com/109619685/183461263-268b0fe8-2853-4ceb-99c1-f91f9b014f9a.png)

## WHat is the FRMP average for juvenile court schools 
1. Use the isolated juvenile court schools data 
2. Make a pivot table and add their % of eligible for FRMP 
3. Get the average of the juvenile court schools by using the average or AVG in the values section 
![eligib count](https://user-images.githubusercontent.com/109619685/183462811-3ce41664-2c92-435e-8136-daa5d6df799e.png)

## Which counties have the biggest difference between the percentage of free and reduced lunch eligible students of their juvenile court schools and the rest of the schools?
1. Create a data set without the juvenile schools 
2. go to main data set, make a copy of that and turn on the filter with only the juvenile schools and then delete them
3. then use that data set to create a pivot table 
4. use the county name, and code as the column and then the FRMP perccentage as the value 

1. use your isolated juvenile court schools and find the FRMP percentage of the juvenile court schools 
2. Include the county name and code, so that vlookup can use the names to match up in the search key 
3. use the *=vlookup(A2,'County Averages excluding Juvenile Court Schools'!A:C, 3,FALSE)* to find the county averages 
4. Create an equation where it is the difference between Juvenile COurt Schools and the rest of the schools, I did an =C3-D3 and then did that for the whole column 
5. I sorted those values from greated difference to least using the sort (Z to A) in descending order  
![vlookup](https://user-images.githubusercontent.com/109619685/183461779-f1532d5f-cc6d-40d5-98c5-2b2f2c9855b9.png)

This is the [sheet](https://docs.google.com/spreadsheets/d/1cjTfw_7ikak9kbFCEB9wb0kQ2FxuZtXEidRKGVdJUMQ/edit?usp=sharing) I used for the data visualization 
## How do these juvenile court schools compare to other types of schools for eligible free lunches?
1. Using the whole data set, make a pivot table 
2. make the column school type and make the value percent of FRMP eligibility 
3. compare the different school types 
![comparing juvenile court schools and other schools](https://user-images.githubusercontent.com/109619685/183462042-b0a43f99-9e3a-44b6-96f6-deace0ec9fd8.png)
# Data Visualizations 
![w84PP-difference-between-the-free-lunch-of-the-county-average-and-their-juvenile-court-school-](https://user-images.githubusercontent.com/109619685/183431850-4c6d9415-e318-463a-8354-612f6cbba2ab.png)
