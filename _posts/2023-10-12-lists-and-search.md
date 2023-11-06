{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "74902a74",
   "metadata": {},
   "source": [
    "---\n",
    "toc: true\n",
    "comments: true\n",
    "layout: post\n",
    "title: List Operations \n",
    "description: SAIGA\n",
    "type: tangibles\n",
    "courses: { compsci: {week: 9} }\n",
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d5459a04",
   "metadata": {},
   "source": [
    "# Made by: Ryan, Daniel, Saaras, Will, and Andrew"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2bb58b0d",
   "metadata": {},
   "source": [
    "## Python lists Operations"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "e7e177fd",
   "metadata": {},
   "source": [
    "### Append function\n",
    "# From the Data Abstractions Unit we Learned about lists and how they can store multiple variables \n",
    "# Today we're going to show you how to add items to lists utilizing the append option"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "133b878d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['hi', 'no']\n"
     ]
    }
   ],
   "source": [
    "\n",
    "lst = [\"hi\"]\n",
    "lst.append(\"no\")\n",
    "print(lst)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7935e94d",
   "metadata": {},
   "source": [
    "### Insert function\n",
    "- The insert function allows you to append items to different lists at a specific location.\n",
    "- Let's first understand how it may work through pseudocode\n",
    "\n",
    "#### Exmaple 1\n",
    "INSERT alist, pos, value \n",
    "INSERT alist, 1, \"hi\" \n",
    "- Here the alist represents your list you want to append an item to\n",
    "- The position is where on the list the item will be generated in respect to the current list\n",
    "- Finally, the value is the item you're adding to your list. \n",
    "- So in the code provided below, in position 1 you insert the item \"hi\" into alist\n",
    "\n",
    "### Your turn!!!!\n",
    "- Turn this pseudocode into python\n",
    "- How may we want to implement this on python? Think back to the data abstraction unit. \n",
    "- ( Hint: Think about the differences between psueodcode and python )"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "cadbfc82",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['hi', 'no', ' maybe']\n"
     ]
    }
   ],
   "source": [
    "# ANSWER: \n",
    "lst = [\"hi\"]\n",
    "lst.append(\"no\") \n",
    "# Inserting items to a specific list, remember python is 0 based on the items!!\n",
    "lst.insert(5, \" maybe\")\n",
    "print(lst)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "0db391f9",
   "metadata": {},
   "source": [
    "### Remove function\n",
    "- The remove functions allows you to remove specific items at a specific position on the list\n",
    "\n",
    "#### Pseudocode example\n",
    "- REMOVE aList, pos\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "2e42ea9b",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['bye']\n",
      "bye\n"
     ]
    }
   ],
   "source": [
    "lst = [\"hi\", \"bye\"]\n",
    "lst.remove(lst[0])\n",
    "print(lst)\n",
    "## You can also access the list by the position, this is called list indexing\n",
    "print(lst[0])"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7f153a9a",
   "metadata": {},
   "source": [
    "### Let's do some Collegeboard exercises\n",
    "- In the following list:\n",
    "  - nums = [65, 89, 92, 35, 84, 78, 28, 75]\n",
    "- Figure out what the minimum number in the list, WITHOUT using the other methods and premade functions.\n",
    "\n",
    "### Second question:\n",
    "- Let's say we have a list called \"animals\" from a survey that stores whether or not they prefer \"cats\" or \"dogs\" as strings in this list.\n",
    "- Transverse this list and tell me the total amount cats and dogs in the list\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "be277539",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "35\n",
      "this number is the lowest number in the nums list\n"
     ]
    }
   ],
   "source": [
    "nums = [65, 89, 92, 35, 84, 78, 28, 75]\n",
    "print(nums[3])\n",
    "print(\"this number is the lowest number in the nums list\")\n",
    "## Your code here"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "6f2ef6ff",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "['cats']\n",
      "only one person works at this petshop and she likes cats.\n"
     ]
    }
   ],
   "source": [
    "animals = [\"cats\", \"dogs\"]\n",
    "\n",
    "animals.remove(\"dogs\")\n",
    "print(animals)\n",
    "print(\"only one person works at this petshop and she likes cats.\")"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a39cbd62",
   "metadata": {},
   "source": [
    "### ITS BINARY SEARCH TIME\n",
    "- By the end of this you should be able to know what binary search is\n",
    "- What the time complexity of binary search is\n",
    "- How to derive the time complexity for binary search"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "82e62d48",
   "metadata": {},
   "source": [
    "### HOW DOES BINARY SEARCH WORK\n",
    "- pay attention to the demonstration in the front\n",
    "- volunteers will be called up\n",
    "- candy if you participate"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "94292a7a",
   "metadata": {},
   "source": [
    "Binary search is like a guessing game where you halve your options at each step. Imagine you're finding a name in a phone book:\n",
    "\n",
    "1. **First Step:** You open the book in the middle.\n",
    "2. **Second Step:** Is the name before or after the middle? You eliminate half of the remaining names.\n",
    "3. **Repeat:** Keep dividing until you find the name or run out of names to check.\n",
    "4. **MAKE SURE YOUR LIST IS SORTED** Binary search will not work if the list isn't sorted\n",
    "\n",
    "Because you're halving the options each time, it's super quick. If you have \\(n\\) names, it takes at most \\( \\log_2(n) \\) steps to find a name. This efficiency, where the time it takes doesn't increase much as the number of names in the phone book grows, is what makes binary search awesome! Binary search is also more optimal for searcihng compared to a linear search for anything that doesnt include small lists..\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "92b4e9ea",
   "metadata": {},
   "source": [
    "### Demo Being shown above\n",
    "The sorted list we have currently, has integers [1, 3, 4, 5, 13, 20], we are currently trying to find the index of the the integer 1 within the list\n",
    "\n",
    "How it works is we start at element 0 for our left position and element 5 for our rightwards position\n",
    "\n",
    "Our middle position becaomes 5 because ((5+0)//2)=3 so element 3\n",
    "\n",
    "Our element 3 within the list gives us the integer 5\n",
    "\n",
    "We then realize that oh 5 is greater then 3 so we have to move leftwards\n",
    "\n",
    "Then to make the algorithm more efficient we move the r backwards 1 beacuse we have already checked at this point\n",
    "\n",
    "So now we can reduce the list to [1, 3, 4]\n",
    "\n",
    "Now we can repeat the same steps as before and find the middle of this list which is 3\n",
    "\n",
    "We realize thats not equivalent to the integer 1, and our value is still too great\n",
    "\n",
    "So we move the middle leftwards 1 positioon\n",
    "\n",
    "AND BAM THATS HOW YOU CAN DO BINARY SEARCH\n",
    "\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "12f650b1",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "1\n"
     ]
    }
   ],
   "source": [
    "#example of binary search in python has a time complexity of O(n)\n",
    "def binarySearch(arr, x):\n",
    "    l= 0 #our minimum element\n",
    "    r=len(arr) - 1 # our maximum element\n",
    "    while l <= r:\n",
    "        mid = l + (r - l) // 2 \n",
    "        if arr[mid] == x:\n",
    "            return mid\n",
    "        elif arr[mid] < x:\n",
    "            l = mid + 1\n",
    "        else:\n",
    "            r = mid - 1\n",
    "    return -1\n",
    "\n",
    "\n",
    "sorted_list = [2, 5, 8, 12, 16]\n",
    "target = 3\n",
    "result = binarySearch(sorted_list, 5)\n",
    "print(result)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "dbe4ce22",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "1\n"
     ]
    }
   ],
   "source": [
    "#Linear Search Approach in O(n)\n",
    "def linear_search(target, sorted_list):\n",
    "    for o in range(len(sorted_list)):\n",
    "        if sorted_list[o]==target:\n",
    "            return(o)\n",
    "#Does not have to be a sorted list for the sake of comparison I just made it sorted\n",
    "sorted_list = [1, 3, 5, 7, 9, 11, 13, 15]\n",
    "target = 3\n",
    "result = linear_search(target, sorted_list)\n",
    "print(result)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4b30f107",
   "metadata": {},
   "source": [
    "Using linear search make a list with elements [\"eggs\", \"milk\", \"butter\", \"cake\"]\n",
    "Then randomize an element 1-4 within that list and find the index of it via linear search"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "6b534051",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "List of items: ['eggs', 'milk', 'butter', 'cake']\n",
      "Random item: cake\n",
      "Index of the random item 'cake': 3\n"
     ]
    }
   ],
   "source": [
    "#code here\n",
    "\n",
    "import random\n",
    "\n",
    "\n",
    "items = [\"eggs\", \"milk\", \"butter\", \"cake\"]\n",
    "\n",
    "\n",
    "random_index = random.randint(0, len(items) - 1)\n",
    "random_item = items[random_index]\n",
    "\n",
    "\n",
    "def linear_search(target, lst):\n",
    "    for index, item in enumerate(lst):\n",
    "        if item == target:\n",
    "            return index\n",
    "    return -1 \n",
    "\n",
    "index = linear_search(random_item, items)\n",
    "\n",
    "\n",
    "print(\"List of items:\", items)\n",
    "print(f\"Random item: {random_item}\")\n",
    "if index != -1:\n",
    "    print(f\"Index of the random item '{random_item}': {index}\")\n",
    "else:\n",
    "    print(f\"The random item '{random_item}' was not found in the list.\")"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4eb89d32",
   "metadata": {},
   "source": [
    "How big O Notation works in the context works in the case of search methods.\n",
    "\n",
    "Lets first explain for linear search, because linear search only requires a iterative approach all we use is O(n), this is due\n",
    "to the loop infinitely going until it finds the element and then after that it doesnt do anything.\n",
    "\n",
    "However binary search is special in this sense because you don't actually have to go through an entire loop how you can picture this is by imagining a list with 1000000 integer values in it and my target value is 59223, binary search makes it so that you just divide the list by 2 until you find the element. It's a lot faster then the iterative approach, where I keep going until I get to 59223 what this does is it allows me to speed up the time and memory usage I take. because I keep dividing the list by 2 allowing for me to form a logarithm because its just repetitive multiplication of 1/2 and then that makes it so that O(log(n)) becomes the time complexity for the Binary search algorithm.\n",
    "\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "51bc29c8",
   "metadata": {},
   "source": [
    "HW TIME!!!!!!!!!!!!!!!!!!\n",
    "We want you guys to make a guessing game below, where utilizing binary search you can within a list of 100 sorted elemments find, a value that your code will randomize using random.randint(). We want you to also make it so every iteration output the number is higher up or lower until you actually get to the answer. We also want number of tries it took to guess the number. Points will be awarded for customizations and potential changes.\n",
    "\n",
    "Extra credit (for above 95%): Send a screenshot on me to slack showing you can do this: https://codeforces.com/contest/1201/problem/C"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "352fbb5e",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Try to guess the target number between 1 and 100.\n",
      "Guess #1: 50\n",
      "The target number is higher.\n",
      "Guess #2: 75\n",
      "The target number is lower.\n",
      "Guess #3: 62\n",
      "The target number is lower.\n",
      "Guess #4: 56\n",
      "The target number is higher.\n",
      "Guess #5: 59\n",
      "Congratulations! The target number 59 was found in 5 tries.\n"
     ]
    }
   ],
   "source": [
    "def generate_fibonacci_sequence(n):\n",
    "    sequence = [1, 1] \n",
    "    while len(sequence) < n:\n",
    "        next_term = sequence[-1] + sequence[-2]\n",
    "        sequence.append(next_term)\n",
    "    return sequence\n",
    "\n",
    "num_terms = int(input(\"Enter the number of Fibonacci terms to generate: \"))\n",
    "fib_sequence = generate_fibonacci_sequence(num_terms)\n",
    "print(fib_sequence)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1d8103b7",
   "metadata": {},
   "source": [
    "HW Part 2: This time instead of utilizing binary search to do it I want you to use linear search to get to the same value and I want you to output the number of iterations it took to get there. Aswell as a congrats message upon getting there points will be awarded upon creativity and completion."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "f7e85aad",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Try to guess the target number between 1 and 100.\n",
      "Guess #1: 1\n",
      "Guess #2: 2\n",
      "Guess #3: 3\n",
      "Guess #4: 4\n",
      "Guess #5: 5\n",
      "Guess #6: 6\n",
      "Guess #7: 7\n",
      "Guess #8: 8\n",
      "Guess #9: 9\n",
      "Guess #10: 10\n",
      "Guess #11: 11\n",
      "Guess #12: 12\n",
      "Guess #13: 13\n",
      "Guess #14: 14\n",
      "Guess #15: 15\n",
      "Guess #16: 16\n",
      "Guess #17: 17\n",
      "Guess #18: 18\n",
      "Guess #19: 19\n",
      "Guess #20: 20\n",
      "Guess #21: 21\n",
      "Guess #22: 22\n",
      "Guess #23: 23\n",
      "Guess #24: 24\n",
      "Guess #25: 25\n",
      "Guess #26: 26\n",
      "Guess #27: 27\n",
      "Guess #28: 28\n",
      "Guess #29: 29\n",
      "Guess #30: 30\n",
      "Guess #31: 31\n",
      "Guess #32: 32\n",
      "Guess #33: 33\n",
      "Guess #34: 34\n",
      "Guess #35: 35\n",
      "Guess #36: 36\n",
      "Guess #37: 37\n",
      "Guess #38: 38\n",
      "Guess #39: 39\n",
      "Guess #40: 40\n",
      "Guess #41: 41\n",
      "Guess #42: 42\n",
      "Guess #43: 43\n",
      "Guess #44: 44\n",
      "Guess #45: 45\n",
      "Guess #46: 46\n",
      "Guess #47: 47\n",
      "Guess #48: 48\n",
      "Guess #49: 49\n",
      "Guess #50: 50\n",
      "Guess #51: 51\n",
      "Guess #52: 52\n",
      "Guess #53: 53\n",
      "Guess #54: 54\n",
      "Guess #55: 55\n",
      "Guess #56: 56\n",
      "Guess #57: 57\n",
      "Guess #58: 58\n",
      "Guess #59: 59\n",
      "Guess #60: 60\n",
      "Guess #61: 61\n",
      "Guess #62: 62\n",
      "Guess #63: 63\n",
      "Guess #64: 64\n",
      "Guess #65: 65\n",
      "Guess #66: 66\n",
      "Guess #67: 67\n",
      "Guess #68: 68\n",
      "Guess #69: 69\n",
      "Congratulations! The target number 69 was found in 69 tries.\n"
     ]
    }
   ],
   "source": [
    "def calculate_mean(data):\n",
    "    return sum(data) / len(data)\n",
    "\n",
    "def calculate_median(data):\n",
    "    sorted_data = sorted(data)\n",
    "    n = len(sorted_data)\n",
    "    if n % 2 == 1:\n",
    "        return sorted_data[n // 2]\n",
    "    else:\n",
    "        mid1 = sorted_data[n // 2 - 1]\n",
    "        mid2 = sorted_data[n // 2]\n",
    "        return (mid1 + mid2) / 2\n",
    "\n",
    "def calculate_mode(data):\n",
    "    mode_dict = {}\n",
    "    for item in data:\n",
    "        if item in mode_dict:\n",
    "            mode_dict[item] += 1\n",
    "        else:\n",
    "            mode_dict[item] = 1\n",
    "    mode = [k for k, v in mode_dict.items() if v == max(mode_dict.values())]\n",
    "    return mode\n",
    "\n",
    "data = [1, 2, 3, 4, 5, 1, 2, 3, 4, 1]\n",
    "mean = calculate_mean(data)\n",
    "median = calculate_median(data)\n",
    "mode = calculate_mode(data)\n",
    "print(f\"Mean: {mean}\")\n",
    "print(f\"Median: {median}\")\n",
    "print(f\"Mode: {mode}\")\n"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.10.12"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
