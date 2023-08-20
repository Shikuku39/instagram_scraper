# Instagram Account Details Fetcher

## Introduction
Hello! Welcome to the Instagram Account Details Fetcher project. In this project, our goal is to retrieve information from Instagram accounts using Python and the instaloader package. This simple tool allows you to scrape and display details about a user's Instagram account. Let's dive right into it!

## Source Code
```python
# Import the instaloader package
import instaloader

# Create an Instaloader() object
ig = instaloader.Instaloader()

# Take the Instagram username as input from the user
usrname = input("Enter username:")

# Fetch the details of the provided username using the instaloader object
profile = instaloader.Profile.from_username(ig.context, usrname)

# Print the fetched details and store the profile pic of that account
print("Username: ", profile.username)
print("Number of Posts Uploaded: ", profile.mediacount)
print(profile.username + " has " + str(profile.followers) + ' followers.')
print(profile.username + " is following " + str(profile.followees) + ' people')
print("Bio: ", profile.biography)
instaloader.Instaloader().download_profile(usrname, profile_pic_only=True)
```

## Code Explanation

1. Start by installing the `instaloader` package using the command `pip install instaloader`.
2. Import the required package, `instaloader`.
3. Create an `instaloader` object, `ig`.
4. Take the Instagram username as input from the user using `input()`.
5. Using the `Profile.from_username()` method of `instaloader`, fetch all the details of the Instagram user.
6. Display all the fetched results in the console.

## Output

**Note**: In this example, the program accepts an Instagram username as input, retrieves information about the user's profile, and then displays it in the console. Here's an illustration of the program's output when it's executed:

``` Terminal
Enter username: kingtenya39
Username: kingtenya39
Number of Posts Uploaded: 14
kingtenya39 is having 1063 followers.
kingtenya39 is following 980 people
Bio: The happiest of people don't necessarily have the best of everything; they just make the most of everything that comes along their way. ✨💯
Stored ID 25217631142 for profile kingtenya39.
kingtenya39\2023-08-09_23-46-31_UTC_profile_pic.jpg ```


