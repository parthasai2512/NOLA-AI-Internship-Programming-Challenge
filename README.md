# NOLA-AI-Internship-Programming-Challenge

Overview:
We need to accept uploads of photos of people's driver's licenses and extract their name and
the expiration date. If the license has expired, we need to warn the user and reject the
submission.
Challenge:
Create a python 3.10+ proof of concept script using whatever module(s) or APIs work best (do
not use anything that costs you money) to extract the required information from the sample
image. You do not need to accept uploads for this proof of concept. Print a warning or raise an
error about expiration.
Example output:
Run with img1.png
John Sample
Expires: 02/15/2027
Accepted
Run with img2.jpg (may be harder to extract name, so any piece of a name works here)
License Sample
Expires:10/01/2016
Warning: Expired
