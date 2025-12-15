
        ---------------------------------
       -------- S P Y B U S T E R --------
        ---------------------------------

Description: 
         
         This is a simple web directory brute-forcer in (Bash)
         designed for directory and file enumeration on web servers. 
         It performs a basic brute-force discovery of hidden paths by    
         appending words from a user-provided wordlist to a target URL 
         and checking the HTTP response status codes using curl.
         
         
Command-line options:
         
         1). -u <url>: Specifies the base target URL (required; e.g., http://example.com/ – note that paths
         
         2). -w <wordlist>: Path to a text file containing potential directory/file names (one per line; required).
         
         
Brute-force process:
         
         1). Reads each word from the wordlist.
          
         2). Sends a silent HEAD request via curl -sI to $url$word.
          
         3). Extracts the final HTTP status code.
          
         4). Color-coded output for easy scanning:
               
                * Green: 200 OK (likely a valid/existing path).
         
                * Red: 404 Not Found.
         
                * Blue: Other status codes (e.g., 301/302 redirects, 403 Forbidden, 500 errors).
         
                * Yellow: No response or error (e.g., timeout or connection issue).
                
                
[!] Usage :
        
        1). chmod +x your_script.sh  # Make it executable if needed
                     -----------------------
        2). Place it in the /usr/local/bin so you can use it anywhere.
        
        3). ./your_script.sh -u http://target.com/ -w /path/to/wordlist.txt
        
        
        
###########################################################################

Made with love by 0x24e

