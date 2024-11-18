# **Social Network Analysis and Recommendations**

## **Overview**
This project simulates a simplified social network to analyze friendships and provide recommendations based on the number of mutual friends. It is a naive approach to understanding algorithms behind friend recommendations like those used on social media platforms.

The script includes various functions for analyzing and interacting with the social network data. This README provides details on each function and its role within the program.

## **Input Files**

You will be provided with five text files representing different social networks:

net1.txt
net2.txt
net3.txt
net4.txt (subset of real Facebook data)
net5.txt (subset of real Facebook data)
Each file follows the format:

The first line contains an integer representing the number of users.
Subsequent lines list pairs of user IDs (user_u, user_v) representing friendships.
Friendships are symmetric, meaning if user_u is friends with user_v, then user_v is also friends with user_u.

## **Functions**

**create_network(file_name)**

Reads a file and returns a list of tuples representing the network.
Each tuple contains a user ID and a list of friends.
Example:
[(0, [1]), (1, [0,2,8]), (2, [1,3]), (3, [2])]

**getCommonFriends(user1, user2, network)**

Returns a list of common friends between two users.
Example:
getCommonFriends(3, 1, net1) => [0, 9]

**recommend(user, network)**

Recommends a new friend for the given user based on common friends.
Example:
recommend(6, net1) => 7

**k_or_more_friends(network, k)**

Returns a list of users who have at least k friends.
Example:
k_or_more_friends(net1, 5) => [3, 1, 0]

**maximum_num_friends(network)**

Returns the highest number of friends any user has in the network.
Example:
maximum_num_friends(net1) => 9

**people_with_most_friends(network)**

Returns a list of users with the most friends.
Example:
people_with_most_friends(net1) => [1, 2, 8]

**average_num_friends(network)**

Returns the average number of friends per user.
Example:
average_num_friends(net1) => 3.8

**knows_everyone(network)**

Returns True if any user knows all other users, otherwise False.
Example:
knows_everyone(net2) => True

**get_uid(network)**

Prompts the user to enter a valid user ID and handles incorrect inputs.
Example:
get_uid(net1) => Enter an integer for a user ID: 7
