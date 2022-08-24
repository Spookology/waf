green="\x1b[32m\x1b[1m"
red="\x1b[31m\x1b[1m"
reset="\x1b[0m"
import random
import math
import os
os.system("title checks thing")
while True:
  columns=input("Columns:    ")
  rows=input("Rows:       ")
  checks=input("Checks/Row: ")
  try:
    columns=int(columns)
    rows=int(rows)
    checks=int(checks)
  except ValueError:
    print("The columns, rows and checks input must be integers / whole numbers")
    continue
  break

os.system("cls")

while True:
  generatedrows=[]
  for _ in range(rows):
    placestocheck=[]
    for _ in range(checks):
      newcheck=math.ceil(random.random()*columns)
      while newcheck in placestocheck:
        newcheck=math.ceil(random.random()*columns)
      placestocheck+=[newcheck]
    row=""
    for c in range(columns):
      isacheck=False
      for checks2 in placestocheck:
        if c+1 == checks2:
          isacheck=True

      if isacheck:
        row+=f"{green}V{reset} "
      else:
        row+=f"{red}X{reset} "
    generatedrows+=[row]
    
  for row in generatedrows:
    print(row)
  input("\nPress enter to regenerate\n")
  os.system("cls")
