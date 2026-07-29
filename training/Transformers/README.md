# Model 1: DistilBERT + Fine-tuning
___
## Ý nghĩa:
- Logistic Regression: Là phiên bản thu nhỏ của model BERT, Kết hợp giữa mất mát từ mô hình lớn (BERT gốc), kết hợp giữa mất mát từ mô hình lớn (BERT gốc), mất mát mô hình hóa ngôn ngữ và mất mát khoảng cách cosin
---
## Pipeline:
```
Dữ liệu Train / Validation / Test 
        ↓
Chuyển Pandas DataFrame thành Hugging Face Dataset 
        ↓ 
DistilBERT Tokenizer 
        ↓ 
input_ids + attention_mask 
        ↓ 
Pretrained DistilBERT 
        ↓
Classification Head 
        ↓ 
Fine-tuning trên tập Train 
        ↓ 
Đánh giá trên Validation và Test 
        ↓ 
Negative hoặc Positive
```