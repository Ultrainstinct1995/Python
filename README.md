# Python

Algorithm for file updates in Python
Project description
As a Security professional at a healthcare company, I will be tasked with updating files and giving permissions to employees who are able to access patient records and on the other hand I will be having restrictions for those employees who will not be allowed to access those records. I will be using python code to effectively execute this task.
Open the file that contains the allow list
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# First line of `with` statement

with open(import_file, "r") as file:
 
Here we assign the file name to “import file” then we have the “remove_list” to remove the IP addresses that are not to access information and then we use with and open to direct us to the file so that we may have it open as a readable file.

Read the file contents
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build `with` statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

  ip_addresses = file.read()

# Display `ip_addresses`

print(ip_addresses)

Here, We will open the file for the import file to see who had permission to read but with using the .read(), we will be able to read the entire content with the variable stored in the “ip_address” We go ahead and print to se the results of the ip_addresses printed out.
Convert the string into a list
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build `with` statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

  ip_addresses = file.read()

# Use `.split()` to convert `ip_addresses` from a string to a list

ip_addresses = ip_addresses.split()

# Display `ip_addresses`

print(ip_addresses)

Here, We will be splitting the ip addresses and placing commas in between the ip address as a list instead of a string so that we may have it seen organized in a different way.
Iterate through the remove list
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build `with` statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

  ip_addresses = file.read()

# Use `.split()` to convert `ip_addresses` from a string to a list

ip_addresses = ip_addresses.split()

# Build iterative statement
# Name loop variable `element`
# Loop through `ip_addresses`

for element in ip_addresses:

    # Display `element` in every iteration

    print(element)

As shown, Just for this code, we will iterate through the remove list which will have each element as well iterated.
Remove IP addresses that are on the remove list
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build `with` statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

  ip_addresses = file.read()

# Use `.split()` to convert `ip_addresses` from a string to a list

ip_addresses = ip_addresses.split()

# Build iterative statement
# Name loop variable `element`
# Loop through `ip_addresses`

for element in ip_addresses:
  
  # Build conditional statement
  # If current element is in `remove_list`,
  
    if element in remove_list:

        # then current element should be removed from `ip_addresses`

        ip_addresses.remove(element)

# Display `ip_addresses` 

print(ip_addresses)

The code will iterate through the IP address which IP address has elements contained and element also has the remove_list to remove unwanted ip addresses
Adding the .remove() is perfect because there are no duplicates with the ip addresses, if there was, we will see some unexpected behavior.


Update the file with the revised list of IP addresses 
# Define a function named `update_file` that takes in two parameters: `import_file` and `remove_list`
# and combines the steps you've written in this lab leading up to this

def update_file(import_file, remove_list):

    # Build `with` statement to read in the initial contents of the file

    with open(import_file, "r") as file:

        # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

        ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list

    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`

    for element in ip_addresses:

        # Build conditional statement
        # If current element is in `remove_list`,

        if element in remove_list:

            # then current element should be removed from `ip_addresses`

            ip_addresses.remove(element)

    # Convert `ip_addresses` back to a string so that it can be written into the text file 

    ip_addresses = " ".join(ip_addresses)       

    # Build `with` statement to rewrite the original file

    with open(import_file, "w") as file:

        # Rewrite the file, replacing its contents with `ip_addresses`

        file.write(ip_addresses)

Writing a new line we are using the “join” function to join and concatenate new lines for the IP addresses, we are converting the files and then updating the file using .write which will bring out the ip addresses as the line file.

Summary
In summary, I created a Python script that iterates and allows ip addresses to access certain files.. It reads a list of IPs, checks it against another list for removal, and then updates the original file with the changes. I organized the updated list with each IP on a new line. This project not only shows off some Python skills but also demonstrates how automation can simplify tasks, making it a handy tool for anyone dealing with python
