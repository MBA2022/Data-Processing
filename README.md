# 📊 **Improved Data Structure Project Plan**

---

## **1. Project Overview**
This project involves building a system to process and manipulate a recording camera data file.  
**Key Goals**:
- Efficient **data parsing** and **storage**.
- Implement **search, modification, deletion, and compression** functionalities.
- Provide **statistical summaries** of the data.

---

## **2. Features to Implement**

### **A. Core Functionalities**
1. **Data Display**
    - Count and display the **total number of days** in the file.
    - Count and display the **total number of minutes** recorded.
    - Count occurrences of specific values (`1` or `0`).

2. **Data Manipulation**
    - **Delete Values**
        - **Input Format**: `date:startmin:endmin`
        - Deletes values for a specified date and minute range.
    - **Search Values**
        - **Input Format**: `date:startmin:endmin`
        - Retrieves values for a specific date and minute range.
    - **Modify Values**
        - **Input Format**: `date:startmin:endmin:newValues`
        - Replaces values with new data.

3. **Data Compression**
    - Implement **Run-Length Encoding (RLE)** to compress repeated values.
    - Display and compare file sizes **before and after compression**.

---

## **3. Technical Design**

### **A. File Parsing**
- Read the input file line-by-line.
- Extract the **starting date** from the first line.
- Use a **data structure** to store the data for efficient access and manipulation:  
  **Data Structure**: `HashMap<String, int[]>`
    - **Key**: Date as `String`.
    - **Value**: Array of `1440 integers` (1 per minute).

## **B. Implementation Details**

### 1. **Display Methods**
| **Function Name**        | **Description**                          |
|--------------------------|------------------------------------------|
| `countDays()`            | Returns total number of days.           |
| `countMinutes()`         | Returns total minutes recorded.         |
| `countOccurrences(int value)` | Counts occurrences of `1` or `0`.   |

### 2. **Data Manipulation**
| **Function Name**         | **Description**                                    |
|---------------------------|--------------------------------------------------|
| `deleteValues(date, startMin, endMin)` | Deletes data in specified minute range. |
| `searchValues(date, startMin, endMin)` | Retrieves data in specified range.       |
| `modifyValues(date, startMin, endMin, newValues)` | Updates data in range. |

### 3. **Compression**
| **Function Name**        | **Description**                                   |
|--------------------------|-------------------------------------------------|
| `compressData()`         | Compresses data using Run-Length Encoding (RLE).|
| `calculateFileSize()`    | Calculates file size before and after compression.|

---

## **4. Task Division**

| **Task**                                   | **Assigned To**            |
|-------------------------------------------|----------------------------|
| File Parsing (`HashMap` implementation).  | Mohammed Amr               |
| Display methods (`countDays`, `countMinutes`, `countOccurrences`). | Majdi Baradie             |
| Data Manipulation (`deleteValues`, `searchValues`, `modifyValues`). | Mohammed Amr               |
| Compression (`compressData`, `calculateFileSize`). | Majdi Baradie             |
| Report Writing & Examples.                | Both                       |

--- 

## **5. Folder Structure**
```plaintext
CameraDataProcessor/
│
├── CameraDataProcessor.java   # Main program file
├── InputFile.txt              # Sample input data file
└── Report.pdf                 # Report with examples and explanation
```

---

### 📋 **Suggestions for Collaboration**
1. **Frequent Testing**  
   Test each functionality individually to ensure correctness before integration.
2. **Git or Version Control**  
   Use GitHub/Git for tracking changes and collaborating effectively.
3. **Shared Responsibilities**  
   Both team members should review each other's code to ensure mutual understanding and error-checking.

