# Visualise data with Quicksight

### What is Amazon Quicksight?
Amazon Quicksight enables users to create interactive visualisions to analyse
data. It is useful for real-time analytics.

### How I used Amazon Quicksight in this project?
I created a dashboard on Amazon Quicksight to display netflix data. I uploaded
my dataset into an S3 bucket and connected it to Quicksight. I created graphs,
charts to analyse Netflix data (from Kaggle) using Quicksight.

## Upload project files onto S3
S3 is used in this project to store two files, which are the netflix_titles.csv and
manifest.json files.

I edited the manifest.json file by updating the S3 URI of my dataset. Itʼs
important to edit this file by updating the S3 URI to ensure that the file is directing to the right address. 

![Bucket](/netflix-quicksight/src/S3%20Bucket.png)

## Create Quicksight account
It is free to make a Quicksight account as the free trial is for 30 days. I also
enabled Quicksight's access to the specific S3 bucket because that is where my dataset is stored.

![Quicksight Homepage](/netflix-quicksight/src/Quicksight%20Homepage.png)

## Download the dataset
I connected the S3 bucket to QuickSight by creating a **New Dataset**, selecting the checkbox of my manifest.json file in my S3 bucket and copying the S3 URI into the URL field.

The manifest.json file tells QuickSight what your dataset looks like, so QuickSight knows how to understand the data and show it in charts or graphs. Without this map,
QuickSight might get confused and not show the data correctly.

![S3 Connection](/netflix-quicksight/src/S3%20Connection.png)

## My first visualisation
To create visualizations on QuickSight, I dragged relevent fields into the Quicksight
dashboard's AutoGraph space.

The chart shown here is a breakdown of movies vs TV shows per
release year.

![Movies/ TV Shows](/netflix-quicksight/src/Movies:TVshows.png)

I created this graph by putting the release year on the y-axis and making the
type (i.e. movie or TV show) the grouping variable.

## Using filters
Filters are useful for specifying the exact subset of data that you are wanting to
analyse, effectively excluding any irrelevant data.

Here I added a filter by excluding movies and TV shows that were released
before 2015 and specifying the genre. This helped me create a visualisation on movies and TV shows of the three genres, Thrillers, Action & Adevnture and TV Comedies, from 2015 onwards.

![Movies/ TV shows post 2015](/netflix-quicksight/src/Movies:%20Tv%20shows%20post%202015.png)

## Setting up a dashboard
I edited the titles of my graphs so that the purpose of each
chart is clear to the reader. I published my dashboard and used the **Export** function to download my dashboard as a PDF file.

![Dashboard](/netflix-quicksight/src/Dashboard.png)

### Deleting Resources
To avoid any charges for this project, I deleted my bucket and my Quicksight account.

**Thanks to nextwork.org for this project.**