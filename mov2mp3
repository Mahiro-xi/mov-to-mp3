import os
import subprocess

print("mov to mp3 converter")

def convert():
    path = input("Enter the path of the directory: ")
    file_list = os.listdir(path)
    print(file_list)

    for file in file_list:
        if file.endswith(".mov"):
            full_path = os.path.join(path, file)
            print(full_path)
            subprocess.run(["ffmpeg", "-i", full_path, "-vn", "-acodec", "libmp3lame", "-ac", "2", "-ab", "160k", "-ar", "48000", full_path + ".mp3"])
            print("converted to mp3")
        else:
            print("no mov files found in the directory")
            
convert()
