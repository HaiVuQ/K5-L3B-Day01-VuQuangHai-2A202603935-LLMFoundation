# Báo cáo cá nhân — Day 01: Lọc tin nhắn rác bằng ML, DL, Embedding và LLM

> Đổi tên file này thành `MSSV_HoTen.md` của bạn, ví dụ `2A20260000_NguyenVanAn.md`, rồi điền từng mục. Xoá các dòng hướng dẫn in nghiêng khi xong.

- **MSSV: 2A202603935**
- **Họ và tên: Vũ Quang Hải**
- **SEED** (in ở ô đầu notebook): 4124

## 1. Bằng chứng

| Tệp | Có? |
| --- | --- |
| [`day01_lab.ipynb`](day01_lab.ipynb) — notebook đã chạy, còn output | ✅ |
| [`lab1_report.json`](lab1_report.json) — do ô "Báo cáo cuối" sinh ra | ✅ |
| [`hand_calc.jpg`](hand_calc.jpg) — ảnh tính tay có các bước | ✅ |

## 2. Kết quả chính

*Chép bảng so sánh cuối Phần 5 (F1 test, F1 SUB 40, p95 ms/tin, USD/1k tin) của chính bạn.*
                                 precision  recall  F1 (test)  F1 (SUB 40)  \
1. BoW + LogReg (tự code)            1.000   0.856      0.922        0.889   
2. BoW + MLP (deep learning)         0.957   0.918      0.937        0.947   
3a. Encoder (MiniLM) + kNN           0.861   0.959      0.907        1.000   
3b. Encoder (MiniLM) + LogReg        0.968   0.938      0.953        0.974   
3c. Encoder (MiniLM) + MLP head      0.967   0.918      0.942        0.974   
4a. LLM nhỏ zero-shot                0.947   0.900      0.923        0.923   
4b. LLM lớn zero-shot                0.000   0.000      0.000        0.000   
4c. LLM nhỏ few-shot                 1.000   0.900      0.947        0.947   

                                 train (s)  tin/s (cả lô)  p50 ms/tin  \
1. BoW + LogReg (tự code)            4.898   8.462661e+03       0.057   
2. BoW + MLP (deep learning)         9.525   2.577403e+04       0.289   
3a. Encoder (MiniLM) + kNN          82.765   2.565900e+01      50.789   
3b. Encoder (MiniLM) + LogReg       83.169   3.304500e+01      32.359   
3c. Encoder (MiniLM) + MLP head     83.799   3.516300e+01      41.362   
4a. LLM nhỏ zero-shot                0.000   1.372000e+00     547.947   
4b. LLM lớn zero-shot                0.000   4.000000e+10       0.000   
4c. LLM nhỏ few-shot                 0.000   1.300000e+00     626.019   

                                 p95 ms/tin  USD / 1k tin  
1. BoW + LogReg (tự code)             0.122         0.000  
2. BoW + MLP (deep learning)          0.454         0.000  
3a. Encoder (MiniLM) + kNN           65.923         0.000  
3b. Encoder (MiniLM) + LogReg        52.078         0.000  
3c. Encoder (MiniLM) + MLP head      57.607         0.000  
4a. LLM nhỏ zero-shot              2023.297         1.297  
4b. LLM lớn zero-shot                 0.000         1.962  
4c. LLM nhỏ few-shot               2093.902         1.333

## 3. Dự đoán và thực tế

*Chọn 3 dự đoán `predict(...)` lệch nhiều nhất so với kết quả. Mỗi cái: bạn đoán gì, ra gì, vì sao lệch.*

## 4. Phân tích 50 case khó

*Model nào tụt nhiều nhất, ở nhóm case nào? Nêu 2 case cụ thể và cơ chế khiến model sai.*

## 5. Thử thách cá nhân

*Đề theo SEED của bạn, cách làm, kết quả, giải thích.*

## 6. Phương án cho sản phẩm thật

*Với yêu cầu p95 < 50 ms/tin cho 10 triệu SMS/ngày: chọn phương án nào, dẫn số liệu nào, chấp nhận đánh đổi gì.*

## 7. AI log và điều đã học

*Mỗi lần dùng AI: hỏi gì, nhận gì, bạn sửa gì. Sau đó 2–3 câu: điều bạn hiểu ra hôm nay mà trước đó chưa hiểu.*
