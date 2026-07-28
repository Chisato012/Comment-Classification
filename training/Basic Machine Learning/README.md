# Model 1: Logistic Regression và TF-IDF
___
## Ý nghĩa:
- Logistic Regression: Thuật toán phân loại được dùng để gán các đối tượng cho 1 tập hợp giá trị rời rạc  
*<small>(Sử dụng hàm sigmoid để đưa ra đánh giá theo xác suất)</small>*
- TF-IDF: Trích xuất đặc trưng (feature extraction) được dùng để đánh giá mức độ quan trọng của một từ  
*<small>TF (Term Frequency): Đo lường tần suất một từ xuất hiện trong một văn bản cụ thể (Từ xuất hiện nhiều sẽ có điểm TF cao)  
IDF (Inverse Document Frequency): Đo lường mức độ phổ biến của từ đó trong toàn bộ tập hợp các văn bản</small>*
---
## Pipeline:
```
Review
  ↓
TF-IDF
  ↓
Vector số
  ↓
Logistic Regression
  ↓
Positive / Negative
```