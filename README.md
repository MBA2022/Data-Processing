# 📊 **Data Structure Project Plan**

---

## **1. Project Overview**
This project focuses on processing and manipulating data from a recording camera file.  
Key tasks include:
- **Reading and parsing** the file.
- **Displaying statistics** about the data.
- **Searching, modifying, and deleting** specific values.
- **Compressing the file** to reduce its size.

---

## **2. Features to Implement**

### 📌 **Core Functionalities**
1. **Data Display**
    - Total number of **days** in the file.
    - Total number of **minutes** recorded.
    - Count of specific values (`1` or `2`).

2. **Data Manipulation**
    - **Delete Values**  
      Format: `date:startmin:endmin`  
      Deletes data in the specified range of minutes.
    - **Search Values**  
      Format: `date:startmin:endmin`  
      Retrieves the values between the specified range.
    - **Modify Values**  
      Format: `date:startmin:endmin:newValues`  
      Replaces values with new data.

3. **Data Compression**
    - Implement **Run-Length Encoding (RLE)** to compress repeated values.
    - Compare and display file sizes **before and after compression**.

---

## **3. Project Steps**

### 🚀 **Step 1: File Parsing**
- Read the file line by line.
- Extract the first line as the **starting date**.
- Store the data in an efficient data structure:
    - **Data Structure**: `HashMap<String, int[]>`
        - **Key** → Date
        - **Value** → Array of 1440 integers (1 per minute).

---

### ⚙️ **Step 2: Feature Implementation**

#### **1. Display Methods**
| Function Name           | Description                            |
|-------------------------|----------------------------------------|
| `countDays()`           | Returns the total number of days.     |
| `countMinutes()`        | Returns the total minutes recorded.   |
| `countOccurrences(int value)` | Counts occurrences of `1` or `2`. |

#### **2. Data Manipulation**
| Function Name               | Description                                             |
|-----------------------------|---------------------------------------------------------|
| `deleteValues(date, startMin, endMin)` | Deletes data from `startMin` to `endMin`.        |
| `searchValues(date, startMin, endMin)` | Retrieves values from `startMin` to `endMin`.    |
| `modifyValues(date, startMin, endMin, newValues)` | Updates values in the specified range. |

#### **3. Compression**
| Function Name            | Description                                   |
|--------------------------|-----------------------------------------------|
| `compressData()`         | Compresses data using Run-Length Encoding.   |
| `calculateFileSize()`    | Calculates and compares file sizes.          |

---

### 📂 **Step 3: Folder Structure**
```plaintext
CameraDataProcessor/
│
├── CameraDataProcessor.java   # Main program file
├── InputFile.txt              # Sample input data file
└── Report.pdf                 # Report with examples and explanation
