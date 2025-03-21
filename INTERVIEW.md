# 2nd Round Interview Task: API Development for Search and Filter with Pagination

Welcome to the **API Development for Search and Filter with Pagination** task!

This repository serves as the foundation for your project submission and collaboration throughout the 2nd Round Interview Task.

## Task Overview

The goal of this task is to develop a functional and innovative web application feature. Whether you're focusing on:

- **Frontend development with API integration**
- Developing a **complete web application**

We encourage you to demonstrate your skills and creativity in solving the problem at hand. 

## Instructions

1. **API Integration**:  
   - The APIs for fetching search data and applying filters are provided through links in the **`interview.md`** file.
   - Your task is to integrate these APIs into the Next.js frontend application.
   - Ensure that the filter API dynamically updates the results when users apply any filters.

2. **Pagination**:  
   - Implement pagination on the frontend to display the data in manageable chunks (e.g., 10, 20, or 50 items per page), based on the API's response.

3. **Submission**:  
   - Once the task is completed, submit a pull request with your solution to this repository.

## Project Structure

- This repository contains the **`interview.md`** file with detailed instructions, along with links to the provided APIs.
- There is no base code in this repository; you are expected to integrate the APIs into your Next.js project.
- Ensure that you follow all guidelines and structure your code neatly.
- The task is time-sensitive, so please complete and submit your pull request within the given timeframe.

Good luck, and we look forward to seeing your solution!

# Project Details

## Project Repo Link
- **Repository Link**:  
  [https://github.com/Rated/TheSquare-Hackathon-2025](https://github.com/Rated/TheSquare-Hackathon-2025)

## Preferred Languages and Technologies
- **NextJS**

## API Details

### API Links:

- **For Page Data**:  
  ```bash
  https://www.thesqua.re/api/sample/latest/data/search?city=london
  ```

-  **For Page filter**:
```bash
https://www.thesqua.re/api/sample/latest/filter/search?city=london
```

## API Details

- The above API works with query parameters. In the examples provided, the `city` parameter is used to fetch data specific to a city (e.g., London). By default, these APIs fetch the first 15 items.

### For Rent Filter:
To apply the rent filter, you need to pass the `rent_min` and `rent_max` parameters, and specify the default currency as `GBP` in the `curr` parameter.

```bash
&rent_min=76&rent_max=1799&curr=GBP
```

### For Bedroom Filter:
To filter by the number of bedrooms, use the `num_bedroom` parameter. The possible values are:

- `-1` for Studio
- `1` for One Bed
- `2` for Two Bed
- `3` for Three Bed
- `4` for Four Bed
- `5` for Five Bed, and so on.

- For a single Bedroom:
```bash
&num_bedroom=-1
```
- For multiple Bedroom:
```bash
&num_bedroom=-1&num_bedroom=1&num_bedroom=2
```

### For Popular Neighborhoods Filter:
To filter by neighborhood, use the `suburb` parameter. You can filter by a single neighborhood or multiple neighborhoods:

- For a single neighborhood:
```bash
&suburb=london/kensington
```

- For multiple neighborhoods:
  ```bash
  &suburb=london/kensington&suburb=london/south-kensington
  ```

###   For Essentials Filters:
To filter by amenities, you can apply a single or multiple filters:

- **For a single filter**:
  ```bash
  &amenities=fridge-freezer-type

-  **For multiple filters**:
```bash
&amenities=fridge-freezer-type&amenities=wi-fi
```

### Sorting
-  You should show a Sort filter at the top of the page. The available sorting options are as follows:
There are multiple ways of sorting:

- **Relevance**:  
```bash
sort=_score desc
```

-  **Most Booked**: 
  ```bash
  sort=booking_count_full desc
```

-  **Price (Low to High)**:
```bash
   sort=rent asc
```
-  **Price (High to Low)**:
```bash
sort=rent desc
```

-  **Distance**:
```bash
sort=distance asc
```

### Pagination
For pagination, use the `start` parameter to determine the starting point for each set of results:

- For the first 15 records, no additional parameters are needed.
- For the next 15 records:
  ```bash
  &start=15
  ```
-  For the following 15 records:

```bash
&start=30
```

-  For each subsequent set of 15 records, increment the start value by 15 (e.g., start=45, start=60, etc.).

### Extra Query Parameters with Every Request
Include the following query parameters for the user's context:

```bash
&current_user_city=NewDelhi&current_user_ip=122.187.4.250&current_user_country=India
```
-  current_user_city: The city of the user.
-  current_user_ip: The IP address of the user.
-  current_user_country: The country of the user.

### TASK Details:

-   **Search Page Design with API Integration**

<a href="resource/Task1-SearchPage/1-Search-Page-Card-View.pdf" target="_blank">**Open PDF - Card Design**</a>


## How to Get Started

1. **Fork this Repository**:
   - Click on the "Fork" button at the top right of this repository to create a copy of it in your GitHub account.

2. **Clone Your Fork**:
   - Clone the forked repository to your local machine:
     ```bash
     git clone https://github.com/your-username/hackathon-repo.git
     ```

3. **Start Development**:
   - Make changes and build your application.

## How to Submit

1. **Create a Branch**:
   - Once you have developed your features, create a branch to submit your code.
     ```bash
     git checkout -b feature/your-feature-name
     ```
2. **Add Contact Information**:
    - Add your contact details (email, phone number, LinkedIn, etc.) in a file named `yourname-README.md` in the root of your project. This will help us contact you if needed.

3. **Create a Project-README.md**:
    - Create a new `README.md` file for your project where you can provide details about what you have developed. Include the following:
        - **Project Description**: A brief overview of the features you implemented.
        - **How to Test the Application**: Provide detailed instructions on how to run and test the application on our system. For example:
            - Dependencies installation (e.g., Node.js, Python packages)
            - Running the application (e.g., `npm start`, `python app.py`)
            - Any specific configurations required (e.g., environment variables)

4. **Commit Your Changes**:
   - Commit your changes:
     ```bash
     git add .
     git commit -m "Added feature: [feature-name]"
     ```

5. **Push Your Branch**:
   - Push your branch to your forked repo:
     ```bash
     git push origin feature/your-feature-name
     ```

6. **Create a Pull Request**:
   - Go to your GitHub repository and click on the **Pull Request** button to create a pull request to the main repository.

## Evaluation Criteria

- **Code Quality**: Clean, maintainable, and well-commented code.
- **Functionality**: Features implemented as per project requirements.
- **Creativity**: Extra features and unique implementations.
- **UI/UX Design**: User-friendly and visually appealing design.
- **Deployment**: Deploy your application so it runs smoothly and can be accessed in a browser. Share the link.

## Contact Us

If you have any questions or need assistance, please refer to the [`contactus-README.md`](./contactus-README.md) file located in the root of this repository. This file contains the contact details for the event organizers and the support team.