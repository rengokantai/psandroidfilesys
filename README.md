# psandroidfilesys
## 2. Introduction to File Sytem
### 1 Persist Storage Options
SharedPreferences
- Store primitive data in key-value pair
File System
- Internal Storage
  - Store private data on device memory
- External Storage
  - Store public data on the shared external storage
SQLite Databases
- Store structured data in a private db
Network Connection
- Store data on the web with your own network server Eg: Cloud Storage

### 2 SharedPreferences, Internal, and External Storage

SharedPreference | Internal External
--- | ---
Stores data internally in XML files in kv pair format | Stores data and files in device storage or external media storage media storage such as SD card
More efficient due to less read, write overload | Less efficient
By default it stores only primitive data types | Can store complex data, media files such as audio video images etc


## 3. Working with Internal Storage
### 1 Introduction and Project Setup
Files are saved on device's internal storage
By default, the saved files are private to application.
- Other apps cannot access the files
- User is also not allowed to access the files
When the app is uninstalled
- The saved files related to the app are also removed from device

### 2 Overview: Write to the Internal Storage
Important Methods
- openFileOutput(String fileName, int mode)
  - It creates a new file if the file does not exist
- write(byte[] dataBytes)
  - Write the data in the form of bytes to a file
- close()
  - Close the FileOutputStream

- openFileOutput(String filename,int mode)
  - int mode
    - MODE_PRIVATE(default)
    - MODE_APPEND
      - If the file already exists then it writes the data at the data at the end of the file
