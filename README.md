def read_file_safely():
    filename = 'sample.txt'

    try:

        with open(filename, 'r') as file:
            print("Reading file content:")
            for i, line in enumerate(file, start=1):
                # .strip() removes the extra newline character at the end of the line
                print(f"Line {i}: {line.strip()}")
        except FileNotFoundError:
        print(f"Error: The file '{filename}' was not found.")
if _name_ == "_main_":
    read_file_safely()


text_to_write = input("Enter text to write to the file: ")
with open("output.txt", "w") as file:
    file.write(text_to_write + "\n")
print("Data successfully written to output.txt.")
print()
text_to_append = input("Enter additional text to append: ")
with open("output.txt", "a") as file:
    file.write(text_to_append + "\n")
print("Data successfully appended.")
print()
print("Final content of output.txt:")
with open("output.txt", "r") as file:
    content = file.read()
    print(content)
