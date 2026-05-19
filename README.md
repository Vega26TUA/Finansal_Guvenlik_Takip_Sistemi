   Projenin Amacı
Geleceğin finansı olan DeFi (Merkeziyetsiz Finans) ekosistemini ve akıllı sözleşmeleri milyarlarca dolarlık hack saldırılarından koruyan hızlı, otonom ve hibrit bir yapay zeka güvenlik kalkanı oluşturmaktır.

Sistem, geleneksel denetimlerin (audit) yavaşlığını ve yüksek maliyetini ortadan kaldırarak; geliştiricilere kodlarını ana ağa (mainnet) yüklemeden önce saniyeler içinde analiz etme imkanı sunar.

   Nasıl Çalışır? (Hibrit Yapay Zeka Mimarisi)
Sistemimiz hızı ve analitik düşünmeyi birleştiren 2 aşamalı bir mimariye sahiptir:

Aşama 1 (Teşhis - Machine Learning): Random Forest sınıflandırıcısı ve TF-IDF vektörizasyonu kullanılarak kod taranır. Sistem, 8 farklı zafiyet sınıfından hangisinin bulunduğunu saniyeler içinde %92 doğrulukla tespit eder.
Aşama 2 (Tedavi - Google Gemini AI): Teşhis edilen zafiyet Google Gemini 2.5 Flash LLM'e aktarılır. Gemini, zafiyetin neden kaynaklandığını bir siber güvenlik uzmanı gibi raporlar ve kodun güvenli halini OpenZeppelin standartlarıyla baştan yazar.
   Veri Seti ve Mühendislik Zekası
Bu projenin en güçlü yanı veri mühendisliğidir. Açık kaynaklı veriler yetersiz olduğu için 1200+ kontrattan oluşan kendi sentetik zafiyet veri setimizi ürettik.

Overfitting (Aşırı Öğrenme) Nasıl Engellendi? Makine öğrenmesi modellerinin sadece spesifik kelimeleri ezberlemesini önlemek için:

Kodlara %90 oranında 'Ortak İskelet' (Shared Skeleton) eklendi.
Çapraz sınıf şaşırtmacaları (Distractors) ve %8 Etiket Gürültüsü (Label Noise) entegre edildi.
Bu sayede modelimiz kelimeleri ezberlemek yerine, gerçekten kodun algoritmik yapısını analiz etmeyi öğrendi.
   Kullanılan Teknolojiler
Makine Öğrenmesi: Python, Scikit-Learn, Pandas (Random Forest, TF-IDF)
Generative AI: Google Gemini 2.5 Flash API
Kullanıcı Arayüzü: Jupyter Notebook / ipywidgets
   Dosya Yapısı
vulnerability_model.pkl: Eğitilmiş Random Forest ML modeli.
vectorizer.pkl: TF-IDF metin dönüştürücü.
label_encoder.pkl: Sınıf etiketleyici.
smart_contract_dataset.csv: 1200 örnekli sentetik veri seti.
main_notebook.ipynb: Arayüzün ve analiz sisteminin çalıştığı ana dosya.
   Nasıl Çalıştırılır?
Google Colab üzerinde main_notebook.ipynb dosyasını açın.
.pkl uzantılı model dosyalarını Colab'a yükleyin.
Colab "Secrets" kısmına GEMINI_API_KEY anahtarınızı ekleyin.
Hücreleri çalıştırıp test kutusuna Solidity kodunuzu yapıştırın!
