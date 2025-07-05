  try:
      with open('sample.txt', 'r') as file:
          for line in file:
              print(line.strip())
  except FileNotFoundError:
      print("Error: The file 'sample.txt' does not exist.")


    user_input = input("Enter some data to write to the file: ")
  
  # Write user input to the file
  with open('output.txt', 'w') as file:
      file.write(user_input + '\n')
  
  # Append additional data
  with open('output.txt', 'a') as file:
      file.write("Additional data appended.\n")
  
  # Read and display the final content
  with open('output.txt', 'r') as file:
      print("Final content of the file:")
      print(file.read())
  
