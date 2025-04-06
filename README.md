def read_and_modify_file(input_filename, output_filename):
    try:
        with open(input_filename, 'r') as infile:
            content = infile.read()
        
        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()
        
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)
        
        print(f"File '{input_filename}' has been read and modified content written to '{output_filename}'.")
    
    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print(f"Error: The file '{input_filename}' cannot be read.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

if __name__ == "__main__":
    input_filename = "C:\Users\70000920\OneDrive - UPL Limited\Documents\MIS\CSP Adjustments\AME - SOP - FY 25_26"
    output_filename = "C:\Users\70000920\OneDrive - UPL Limited\Documents\MIS\CSP Adjustments\AME - SOP - FY 25_26"
    read_and_modify_file(input_filename, output_filename)
