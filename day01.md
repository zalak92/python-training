Here’s your complete day01.md file:

# Day 1: Variables, Data Types & Strings

> Time: 2-3 hours  
> Goal: Understand how Python stores and handles data

---

## 1.1 What Are Variables?

Variables are labels that store data. Like a box with a name tag.

```python
# Creating variables - no special keyword needed
server_name = "web-server-01"
cpu_cores = 4
memory_gb = 16.0
is_running = True

# Print them
print(server_name)
print(cpu_cores)
print(memory_gb)
print(is_running)

Naming Rules

# GOOD names
server_name = "web-01"
total_cost = 150.0
is_active = True

# BAD names (will cause errors)
# 2server = "web"      ← cannot start with number
# server-name = "web"  ← no hyphens allowed
# class = "web"        ← cannot use reserved words

1.2 Data Types

Python has 4 basic data types:

# String (str) - text inside quotes
hostname = "db-server-01"

# Integer (int) - whole numbers
cpu_count = 8

# Float (float) - decimal numbers
cpu_usage = 72.5

# Boolean (bool) - True or False
is_healthy = True

Check Data Type

hostname = "db-server-01"
cpu_count = 8
cpu_usage = 72.5
is_healthy = True

print(type(hostname))    # <class 'str'>
print(type(cpu_count))   # <class 'int'>
print(type(cpu_usage))   # <class 'float'>
print(type(is_healthy))  # <class 'bool'>

1.3 Type Conversion

# String to Integer
port_str = "8080"
port_num = int(port_str)
print(port_num + 1)  # 8081

# Integer to String
count = 5
message = "Servers: " + str(count)
print(message)  # Servers: 5

# String to Float
usage = "72.5"
usage_num = float(usage)
print(usage_num)  # 72.5

# Float to Integer (removes decimal)
value = 72.9
print(int(value))  # 72

1.4 Basic Math Operations

a = 10
b = 3

print(a + b)   # 13  Addition
print(a - b)   # 7   Subtraction
print(a * b)   # 30  Multiplication
print(a / b)   # 3.33 Division (always float)
print(a // b)  # 3   Floor division (no decimal)
print(a % b)   # 1   Modulus (remainder)
print(a ** b)  # 1000 Power (10 to the power 3)

Real World Example

# Calculate monthly server cost
hourly_rate = 0.0416
hours_per_day = 24
days_per_month = 30

monthly_cost = hourly_rate * hours_per_day * days_per_month
print(f"Monthly cost: ${monthly_cost:.2f}")
# Output: Monthly cost: $29.95

1.5 Strings - The Basics

# Three ways to create strings
name1 = 'web-server'
name2 = "db-server"
name3 = """This is a
multi-line string"""

print(name1)
print(name2)
print(name3)

String Concatenation (Joining)

first = "web"
second = "server"
combined = first + "-" + second
print(combined)  # web-server

String Length

hostname = "web-server-01"
print(len(hostname))  # 13

1.6 String Methods

hostname = "Web-Server-01"

print(hostname.upper())       # WEB-SERVER-01
print(hostname.lower())       # web-server-01
print(hostname.replace("01", "02"))  # Web-Server-02
print(hostname.startswith("Web"))    # True
print(hostname.endswith("01"))       # True
print(hostname.count("-"))           # 2

Split and Join

# Split - break string into list
ip = "192.168.1.100"
parts = ip.split(".")
print(parts)  # ['192', '168', '1', '100']

# Join - combine list into string
servers = ["web-01", "web-02", "web-03"]
result = ", ".join(servers)
print(result)  # web-01, web-02, web-03

1.7 F-Strings (Most Important!)

F-strings let you put variables inside strings easily.

server = "web-server-01"
cpu = 72.5
status = "running"

# OLD way (don't use)
msg = "Server " + server + " CPU: " + str(cpu) + "%"

# NEW way - f-strings (use this!)
msg = f"Server {server} CPU: {cpu}%"
print(msg)
# Output: Server web-server-01 CPU: 72.5%

F-String Formatting

cost = 1234.5678
name = "web-server-01"

# Round to 2 decimal places
print(f"Cost: ${cost:.2f}")
# Output: Cost: $1234.57

# Padding/alignment
print(f"Server: {name:<20} Status: OK")
print(f"Server: {name:>20} Status: OK")
# Left aligned:  Server: web-server-01        Status: OK
# Right aligned: Server:        web-server-01 Status: OK

1.8 String Indexing and Slicing

hostname = "web-server-01"
#           0123456789...

# Indexing (get one character)
print(hostname[0])    # w
print(hostname[4])    # s
print(hostname[-1])   # 1 (last character)
print(hostname[-2])   # 0

# Slicing (get a portion)
print(hostname[0:3])   # web
print(hostname[4:10])  # server
print(hostname[-2:])   # 01
print(hostname[:3])    # web (from start)

1.9 Practice Exercises
Exercise 1: Server Info Card

# Create these variables and print a formatted card
# server_name = "prod-db-01"
# ip_address = "10.0.2.15"
# cpu_cores = 16
# memory_gb = 64
# disk_gb = 500
# monthly_cost = 450.00
# is_running = True

# Expected Output:
# ================================
# SERVER INFORMATION CARD
# ================================
# Name:    prod-db-01
# IP:      10.0.2.15
# CPU:     16 cores
# Memory:  64 GB
# Disk:    500 GB
# Cost:    $450.00/month
# Status:  Running
# ================================

Exercise 2: Cost Calculator

# Given these values:
# instances = 5
# hourly_rate = 0.0416
# hours_in_month = 720
# discount_percent = 10

# Calculate:
# 1. Cost per instance per month
# 2. Total cost before discount
# 3. Discount amount
# 4. Final cost after discount
# Print each with proper formatting

Exercise 3: IP Address Parser

# Given: ip = "192.168.1.100"
# Extract and print:

continue
NTT Logo

Continuing day01.md from where it stopped:

### Exercise 3: IP Address Parser
```python
# Given: ip = "192.168.1.100"
# Extract and print:
# 1. First octet (192)
# 2. Last octet (100)
# 3. Is it a private IP? (starts with 192.168)
# 4. Replace last octet with "0" to get network address

ip = "192.168.1.100"
parts = ip.split(".")

first_octet = parts[0]
last_octet = parts[-1]
is_private = ip.startswith("192.168")
network = ip.rsplit(".", 1)[0] + ".0"

print(f"IP Address:  {ip}")
print(f"First Octet: {first_octet}")
print(f"Last Octet:  {last_octet}")
print(f"Is Private:  {is_private}")
print(f"Network:     {network}")

Exercise 4: String Detective

# Given this log line:
log = "ERROR 2024-01-15 10:23:45 Server web-01 disk usage at 95%"

# Find:
# 1. Length of the log line
# 2. Is it an ERROR log? (check if "ERROR" is in the string)
# 3. Convert to lowercase
# 4. Replace "ERROR" with "WARNING"
# 5. Split into words and print word count

print(f"Length: {len(log)}")
print(f"Is Error: {'ERROR' in log}")
print(f"Lowercase: {log.lower()}")
print(f"Replaced: {log.replace('ERROR', 'WARNING')}")
print(f"Word count: {len(log.split())}")

1.10 Solutions
Solution 1: Server Info Card

server_name = "prod-db-01"
ip_address = "10.0.2.15"
cpu_cores = 16
memory_gb = 64
disk_gb = 500
monthly_cost = 450.00
is_running = True

status = "Running" if is_running else "Stopped"

print("================================")
print("SERVER INFORMATION CARD")
print("================================")
print(f"Name:    {server_name}")
print(f"IP:      {ip_address}")
print(f"CPU:     {cpu_cores} cores")
print(f"Memory:  {memory_gb} GB")
print(f"Disk:    {disk_gb} GB")
print(f"Cost:    ${monthly_cost:.2f}/month")
print(f"Status:  {status}")
print("================================")

Solution 2: Cost Calculator

instances = 5
hourly_rate = 0.0416
hours_in_month = 720
discount_percent = 10

cost_per_instance = hourly_rate * hours_in_month
total_cost = cost_per_instance * instances
discount_amount = total_cost * (discount_percent / 100)
final_cost = total_cost - discount_amount

print(f"Cost per instance/month: ${cost_per_instance:.2f}")
print(f"Total cost (before):     ${total_cost:.2f}")
print(f"Discount ({discount_percent}%):          ${discount_amount:.2f}")
print(f"Final cost:              ${final_cost:.2f}")

1.11 Key Takeaways

    Variables store data - no keyword needed
    Four basic types: str, int, float, bool
    Use type() to check data type
    Use int(), str(), float() to convert types
    F-strings are the best way to format output
    Strings have many useful methods
    Indexing starts at 0
    Slicing uses [start:end]

1.12 Quick Reference Cheat Sheet

# Variables
name = "text"        # string
count = 10           # integer
price = 9.99         # float
active = True        # boolean

# Type check & convert
type(name)           # <class 'str'>
int("5")             # 5
str(5)               # "5"
float("5.5")         # 5.5

# String methods
"hello".upper()      # HELLO
"HELLO".lower()      # hello
"a-b-c".split("-")   # ['a','b','c']
"-".join(['a','b'])   # a-b
"hello".replace("h","H")  # Hello
len("hello")         # 5

# F-strings
f"Name: {name}"
f"Cost: ${price:.2f}"

