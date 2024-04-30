#include <iostream>
#include <string>
#include <cstdlib> 

using namespace std;

int main() {
    
    cout << "Enter the YouTube video ID: ";
    string video_id;
    getline(cin, video_id);
    
    string thumbnail_url = "https://img.youtube.com/vi/" + video_id + "/maxresdefault.jpg";

  
    string output_file = "thumbnail1.jpg";

  
    string command = "wget -O " + output_file + " " + thumbnail_url;

    int status = system(command.c_str());
    

    if (status == 0) {
        cout << "Thumbnail downloaded successfully!" << endl;
    } else {
        cout << "Failed to download thumbnail" << endl;
    }

    return 0;
}

