    written by peteskene@gmail.com
    
    takes in a list of bedfiles ['A.bed', 'B.bed']; can include path
    and counts total number of reads and duplicated reads:
        if all_columns=False, considers only first 3 columns <chr> <start> <end> 
        if all_columns=True, uses all columns of bed file for testing duplicity
        
    generates a new bed file with duplicates removed (keeps first instance of duplicate).
    Auto-generates filenames 'A_unique.bed', 'B_unique.bed'. New files are saved to the parent location
        
    returns a dataframe:
        <bedfile name> <total reads> <duplicates> <% duplicates> <unique bedfile name> <non-duplicated reads>
