
Sentiment based method
Đầu tiên chúng tôi kiểm tra so khớp từ, toxic spans sẽ bao gồm từ tiêu cực hoặc độc
hại. Chúng tôi cũng sử dụng TextBlob (Loria, 2018) để nhận diện cảm xúc của từ. Với
phương pháp so khớp từ, F1-score đạt 0.39. Cuối cùng chúng tôi kết hợp hai phương
pháp(đánh dấu từ độc hại và các từ có cảm xúc tiêu cực là độc hại) và đạt được
F1-score 0.42

Named Entity Recognition model
Chúng tôi nhận định CRF là một vấn đề tương tự NER, do đó toxic span cũng được
xem như một nhãn NER khác. Chúng tôi coi toxic, non-toxic và padding là nhãn và
áp dụng CRF cho tác vụ này. Nhãn padding được thêm vào để giảm sự thiên vị của
mô hình vào lớp non-toxic. Mô hình được huấn luyện gồm 2 epoch với learning rate là
3 ∗ 10−5
