# rename-tool
## simple commandline tool to batch rename files
# functionality
##rename [-options] <folder> [search_string] [prefix]
##Options:
  -n        Match only 2-digit numbers
  
  -b        Match both string and number (e.g. Wano 02)
  
  -s        Strip matched search string from result
  
  -a        Add prefix before the matched part
  
  -d        Just delete the search string from filenames
  
  --dry-run Simulate without renaming

#Examples:
  rename --dry-run -a wano "Wano" "One Piece S1E"
  
  rename -n <folder> "s1e02" --> "02"
  
  - - - - - - - - -  "s1e23" --> "22"
                     
  rename -b <folder> wano "[909-910] Wano 01 [720p]" --> "wano 01"
  
  rename -b <folder> wano "[909-910] Wano 01 [720p]" --> "wano 01"
  
  rename -a <folder> "S1E"  "1.mp4" --> "S1E1.mp4"
  
  rename -d <folder> s1e "s1e02" --> "02"

