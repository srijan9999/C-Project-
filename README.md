#YouTube Thumbnail Downloader
This simple C++ program allows you to download a YouTube video's thumbnail by providing its URL.

*Prerequisites*
To run this program, you need:

A C++ compiler (such as g++ or clang++)
wget utility installed on your system (for downloading the thumbnail)
*How to Use*
Clone or download this repository to your local machine.
Compile the main.cpp file using a C++ compiler. For example:
CSS
Copy code
g++ main.cpp -o youtube_thumbnail_downloader
Run the compiled executable:
bash
Copy code
./youtube_thumbnail_downloader
You can just follow the prompts to enter the YouTube video URL.
The program will download the thumbnail and save it as thumbnail.jpg in the current directory.
Customization
You can modify the isValidYouTubeURL function in the main. cpp to add more robust validation for YouTube video URLs.
Change the output_file variable in the main. cpp to specify a different filename for the downloaded thumbnail.
Note
This program relies on the wget utility to download the thumbnail. Ensure it's installed on your system and accessible from the command line.

Code Explanation 
*Header Inclusions:*
#include <iostream>: Provides input/output stream functionalities.
#include <string>: Provides string manipulation functionalities.
#include <cstdlib>: Provides the system() function for executing system commands.
*Namespace Usage:*
using namespace std: Allows using symbols from the std namespace without prefixing them with std::.
Main Function:
The main() function is the entry point of the program.
*User Input:*
The program prompts the user to enter the YouTube video ID.
The ID is read from the standard input (cin) using getline() and stored in the video_id string variable.
Thumbnail URL Construction:
The URL of the YouTube thumbnail is constructed by concatenating the video ID with the base thumbnail URL (https://img.youtube.com/vi/) and the thumbnail resolution (maxresdefault.jpg).
*Output File Path:*
The output file path (output_file) is set to "thumbnail1.jpg".
Command Construction:
A system command (command) is constructed to download the thumbnail using the wget command-line utility.
The -O option specifies the output file name.
*Thumbnail Download:*
The constructed command is executed using the system() function.
The return value of system() (status) indicates the success or failure of the command execution.
*Status Check:*
If the status is 0, the thumbnail is downloaded successfully, and a success message is printed.
If the status is non-zero, indicating an error, a failure message is printed.
*Program Termination:*
The program exits with a return code of 0 on successful execution and a non-zero code otherwise.
