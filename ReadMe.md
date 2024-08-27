# Peptide Sequence Mutation Generator

## Project Overview

This project generates all possible single-point mutations of the peptide sequence "QVFLSEAF". The generated sequences are useful for studying the effects of amino acid substitutions on peptide-protein interactions, particularly in the context of binding with KLRG-1.

## Installation

To get started, set up your Python environment locally:

Make sure Python is installed ideally python 3x
run code the code python3 in terminal to start the python script

python3

Can now begin running the Code

# Original amino acid sequence
sequence = "QVFLSEAF"

# List of all 20 amino acids
amino_acids = ['A', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'K', 'L', 
               'M', 'N', 'P', 'Q', 'R', 'S', 'T', 'V', 'W', 'Y']

# List to store all possible combinations
combinations = []

# Generate all combinations by replacing one amino acid at a time
for i, original_aa in enumerate(sequence):
    for aa in amino_acids:
        if aa != original_aa:  # Only replace with a different amino acid
            # Create a new sequence with the replacement
            new_sequence = sequence[:i] + aa + sequence[i+1:]
            combinations.append(new_sequence)

# Display the results
for combo in combinations:
    print(combo)

# Optionally, display the total number of combinations
print(f"Total number of combinations: {len(combinations)}")
