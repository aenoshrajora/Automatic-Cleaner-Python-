# Automatic-Cleaner-Python-This program clears your all files and move them to their corresponding folder.
import os

# Making Folders Function
def createIfNotExists(folder):
    if not os.path.exists(folder):
        os.makedirs(folder)

def move(foldername, files):
    for file in files:
        os.replace(file, f"{foldername}/{file}")


files = os.listdir()
files.remove('Automatic_Folder_Cleaner.py')
# Creating Folders
if __name__ == "__main__":

    createIfNotExists('Images')
    createIfNotExists('Exe FIles')
    createIfNotExists('Rar FIles')
    createIfNotExists('Apk FIles')
    createIfNotExists('Videos')
    createIfNotExists('Iso FIles')
    createIfNotExists('html FIles')
    createIfNotExists('docs Files')
    createIfNotExists('Zip Files')

# Listing All Files
    imgExts = [".png", ".jpg", ".jpeg"]
    images = [file for file in files if os.path.splitext(file)[
        1].lower() in imgExts]

    docExts = [".txt", ".docs", ".doc", ".pdf"]
    docs = [file for file in files if os.path.splitext(file)[1].lower() in docExts]

    zipeExts = [".zip"]
    zipe = [file for file in files if os.path.splitext(file)[1].lower() in zipeExts]

    exeExts = [".exe"]
    exe = [file for file in files if os.path.splitext(file)[1].lower() in exeExts]

    rarExts = [".rar"]
    rar = [file for file in files if os.path.splitext(file)[1].lower() in rarExts]

    apkExts = [".apk"]
    apk = [file for file in files if os.path.splitext(file)[1].lower() in apkExts]

    videosExts = [".mp4", ".mov", ".wmv", ".flv",
                ".avi", ".avchd", ".webm", ".mkv"]
    videos = [file for file in files if os.path.splitext(file)[1].lower() in videosExts]

    htmlExts = [".html", ".css", ".js"]
    html = [file for file in files if os.path.splitext(file)[
        1].lower() in htmlExts]

    isoExts = [".iso"]
    iso = [file for file in files if os.path.splitext(file)[1].lower() in isoExts]

     others = []
     for file in files:
         ext = os.path.splitext(file)[1].lower()
         if (ext not in videosExts) and (ext not in isoExts) and (ext not in htmlExts) and (ext not in apkExts) and (ext not in rarExts) and (ext not in imgExts) and (ext not in docExts)  and (ext not in) and (ext not in htmlExts) and (ext not in exeExts):
             others.append(file)
# Moving Files
    move("images", images)
    move("Videos", videos)
    move("Apk Files", apk)
    move("Rar Files", rar)
    move("iso Files", iso)
    move("docs Files", docs)
    move("html Files", html)
    move("Exe Files", exe)
    move("Zip Files", zipe)
