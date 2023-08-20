# Instagram Account Details Fetcher

## Introduction
Hello! Welcome to the Instagram Account Details Fetcher project. In this project, we aim to retrieve information from Instagram accounts using Python and the instaloader package. This simple tool allows you to scrape and display details about a user's Instagram account. Let's dive right into it!

## Source Code
```python
# Import instaloader package
import instaloader

# Creating an Instaloader() object
ig = instaloader.Instaloader()

# Taking the Instagram username as input from the user
usrname = input("Enter username:")

# Fetching the details of the provided username using the instaloader object
profile = instaloader.Profile.from_username(ig.context, usrname)

# Printing the fetched details and storing the profile pic of that account
print("Username: ", profile.username)
print("Number of Posts Uploaded: ", profile.mediacount)
print(profile.username + " is having " + str(profile.followers) + ' followers.')
print(profile.username + " is following " + str(profile.followees) + ' people')
print("Bio: ", profile.biography)
instaloader.Instaloader().download_profile(usrname, profile_pic_only=True)
