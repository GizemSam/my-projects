![alt text](https://blogimages.softwaresuggest.com/blog/wp-content/uploads/2022/03/01151715/Essential-Reasons-to-Choose-Cloud-Based-HR-Software-02.png)

# Employee Churn Analysis
---
### İş Problemi (Business Problem)
- Firma Personellerinin istifa(churn) nedenlerini araştırlması bunun için önlem alınmasını ve şirkete katılan 
veya şirket içindeki olası istifa edecek olan personelleri belirlemek içinbir  makine öğrenme modeli geliştirilmesini isitiyor.
---
# Veri Seti 

- Age: Çalışanın yaşı (sayısal değer)
- Attrition: İşten ayrılma durumu (Yes/Evet veya No/Hayır)
- BusinessTravel: İş seyahati sıklığı (Travel_Rarely/Nadiren seyahat, Travel_Frequently/Sık sık seyahat, Non-Travel/Seyahat etmeme)
- DailyRate: Günlük ücret (sayısal değer)
- Department: Çalışanın çalıştığı departman (Sales/Satış, Research & Development/Araştırma ve Geliştirme, Human Resources/İnsan Kaynakları)
- DistanceFromHome: Evden işe olan mesafe (sayısal değer)
- Education: Eğitim düzeyi (sayısal değer)
- EducationField: Eğitim alanı (Life Sciences/Hayat Bilimleri, Technical Degree/Teknik Lisans, Human Resources/İnsan Kaynakları vb.)
- EmployeeCount: Çalışan sayısı (sabit değer)
- EmployeeNumber: Çalışan numarası (sayısal değer)
- EnvironmentSatisfaction: Çalışma ortamı memnuniyeti (sayısal değer)
- Gender: Cinsiyet (Female/Kadın veya Male/Erkek)
- HourlyRate: Saatlik ücret (sayısal değer)
- JobInvolvement: İşe dahil olma düzeyi (sayısal değer)
- JobLevel: İş seviyesi (sayısal değer)
- JobRole: İş rolü (Sales Executive/Satış Yöneticisi, Research Scientist/Araştırma Uzmanı vb.)
- JobSatisfaction: İş tatmini (sayısal değer)
- MaritalStatus: Medeni durum (Single/Bekar, Married/Evli, Divorced/Boşanmış)
- MonthlyIncome: Aylık gelir (sayısal değer)
- MonthlyRate: Aylık ücret (sayısal değer)
- NumCompaniesWorked: Çalışılan şirket sayısı (sayısal değer)
- Over18: 18 yaşından büyük olma durumu (Y/Evet)
- OverTime: Fazla mesai yapma durumu (Yes/Evet veya No/Hayır)
- PercentSalaryHike: Maaş artış yüzdesi (sayısal değer)
- PerformanceRating: Performans değerlendirmesi (sayısal değer)
- RelationshipSatisfaction: İlişki tatmini (sayısal değer)
- StandardHours: Standart çalışma saati (sabit değer)
- StockOptionLevel: Hisse senedi opsiyon düzeyi (sayısal değer)
- TotalWorkingYears: Toplam çalışma yılı (sayısal değer)
- TrainingTimesLastYear: Geçen yıl yapılan eğitim süresi (sayısal değer)
- WorkLifeBalance: İş-yaşam dengesi (sayısal değer)
- YearsAtCompany: Şirkette geçirilen yıl sayısı (sayısal değer)
- YearsInCurrentRole: Şu anki pozisyonda geçirilen yıl sayısı (sayısal değer)
- YearsSinceLastPromotion: Son terfi üzerinden geçen yıl sayısı (sayısal değer)
- YearsWithCurrManager: Mevcut yöneticiyle çalışılan yıl sayısı (sayısal değer)

---

### Bu projede yapılanlar
- Keşifsel Veri Analizi
- Katagorik değişken Analizi
- Numarik Değişken Analizi
- Eksik Gözlem Analizi
- Aykırı Değer Analizi(Baskılama)
- Base Model Kurulumu
- Özellik Mühendisliği (Feature Engineering)
- Feature Engineering Sonrası Modellerin Kurulması
- Hiperparametre optimizasyonu
- Yeni Değişkenerin Modele Etkisi

---

![alt text](https://editor.analyticsvidhya.com/uploads/27422asda.jpg)

# Feature Engineering


- *Yeni eklenen değişkenlerin anlamları şu şekildedir:

* AgeCategory: Yaşa göre oluşturulan kategorik bir değişken. Genç, Orta Yaşlı ve Yaşlı olmak üzere üç kategoriye ayrılır.

* CloseToHome: Eve yakın olan çalışanları ifade eden bir değişken. DistanceFromHome değişkenine göre belirlenir ve Eve Yakın veya Eve Uzak şeklinde değer alır.

* FarFromHome: Eve uzak olan çalışanları ifade eden bir değişken. DistanceFromHome değişkenine göre belirlenir ve Eve Uzak veya Eve Yakın şeklinde değer alır.

*  NEW_Age_JobLevel: Yaş ile iş seviyesinin çarpımını ifade eden bir değişken. Yaşın ve iş seviyesinin birleşik etkisini yansıtır.

* NEW_Education_JobLevel: Eğitim düzeyi ile iş seviyesinin çarpımını ifade eden bir değişken. Eğitim düzeyinin ve iş seviyesinin birleşik etkisini yansıtır.

* NEW_Age_Distance: Yaş ile evden uzaklık arasındaki çarpımı ifade eden bir değişken. Yaşın ve evden uzaklığın birleşik etkisini yansıtır.

* NEW_Income_Rate: Aylık gelirin aylık oranını ifade eden bir değişken. Aylık gelirin aylık ücret oranıyla bölünmesiyle elde edilir.

* NEW_Years_Companies: Toplam çalışma yılına göre ortalama iş değişikliği sayısını ifade eden bir değişken. Toplam çalışma yılına bölünerek elde edilir.

* NEW_PerformanceScore: Performans puanı ile maaş artış yüzdesinin çarpımını ifade eden bir değişken. Performans puanı ve maaş artış yüzdesinin birleşik etkisini yansıtır.

* NEW_WorkLifeBalance_Score: İş tatmini ile iş-yaşam dengesi puanının çarpımını ifade eden bir değişken. İş tatmini ve iş-yaşam dengesi puanının birleşik etkisini yansıtır.

* OverTime_Distance: Fazla mesai yapma durumu ile eve olan mesafe arasındaki etkileşimi ifade eden bir değişken. Fazla mesai yapma durumuyla eve olan mesafe arasındaki ilişkiyi yakalamayı amaçlar.

* NumCompaniesWorked_MonthlyRate_Ratio: Şirket değiştirme sayısı ile aylık ücret oranının oranını ifade eden bir değişken. Şirket değiştirme sayısının aylık ücret oranına olan etkisini yansıtır.

* PerformanceRating_Age_Difference: Performans puanı ile yaş arasındaki farkı ifade eden bir değişken. Yaşın performans puanına olan etkisini gösterir. Pozitif değerler, yaşın performans puanını olumlu yönde etkilediğini, negatif değerler ise olumsuz yönde etkilediğini gösterir.

* EmployeeNumber_PercentSalaryHike_Ratio: Çalışan numarasının maaş artış yüzdesine olan oranını ifade eden bir değişken. Çalışan numarasının maaş artış yüzdesine olan etkisini yansıtır.

* NEW_TotalWorkingYears_MonthlyIncome: Toplam çalışma yılı ile aylık gelirin çarpımını ifade eden bir değişken. Toplam çalışma yılının aylık gelire olan etkisini gösterir.

* NEW_Income_JobSatisfaction_Multiplication: Aylık gelirin iş tatminiyle çarpımını ifade eden bir değişken. Aylık gelirin iş tatmini üzerindeki etkisini yansıtır.

* NEW_JobSatisfaction_YearsAtCompany_Ratio: İş tatmininin çalışılan yıl sayısına olan oranını ifade eden bir değişken. İş tatmininin çalışılan yıl sayısına olan etkisini gösterir.

* NEW_SatisfactionScore: Çalışanın genel tatmin düzeyini ifade eden bir değişken. JobSatisfaction, EnvironmentSatisfaction ve RelationshipSatisfaction değişkenlerinin ortalaması alınarak elde edilir.

* NEW_MonthlyIncome_Ratio: Aylık gelirin aylık oranını ifade eden bir değişken. Aylık gelirin aylık ücret oranıyla bölünmesiyle elde edilir.

* NEW_AvgYearsPerJob: Toplam çalışma yılına göre ortalama iş değişikliği sayısını ifade eden bir değişken. Toplam çalışma yılına bölünerek elde edilir.

**Bu eklenen değişkenler, farklı özelliklerin etkileşimini ve iş performansı üzerindeki potansiyel etkilerini yansıtmaktadır.**









