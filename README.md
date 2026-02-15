#<a href="https://ods.ai/competitions/data-fusion2026-cybershelf">Data Fusion Contest 2026 - Задача 2 "Киберполка"</a>
<img width="1149" height="443" alt="image" src="https://github.com/user-attachments/assets/61b3ceae-a695-4026-95cc-cc013a10890b" />

10.02.2026 

Метрика задачи позволяет переформулировать задачу из multi-label классификации и получить более мелкие задачи классификации, вплоть до 41 задачи одноклассовой классификации.
Задачи одноклассовой классификации можно решать независимо, разделив их между частниками команд и/или между компьютерами.

0004.ipynb - разбивка на одноклассовые классификации (LB - 0,8181423636386495)

|tcol       |best_iteration|AUC               |rank|
|-----------|--------------|------------------|----|
|target_1_1 |999           |0.911140352487564 |34  |
|target_1_2 |995           |0.7977737188339233|18  |
|target_1_3 |999           |0.8619800209999084|29  |
|target_1_4 |999           |0.8188646733760834|21  |
|target_1_5 |975           |0.8634224236011505|30  |
|target_2_1 |970           |0.7969111204147339|17  |
|target_2_2 |999           |0.9166249632835388|35  |
|target_2_3 |790           |0.8069062829017639|20  |
|target_2_4 |875           |0.7205553948879242|8   |
|target_2_5 |995           |0.7667911052703857|15  |
|target_2_6 |955           |0.7191536724567413|7   |
|target_2_7 |999           |0.935670018196106 |37  |
|target_2_8 |565           |0.97784823179245  |41  |
|target_3_1 |999           |0.6826431155204773|1   |
|target_3_2 |999           |0.9043170511722564|32  |
|target_3_3 |835           |0.7442838549613953|10  |
|target_3_4 |955           |0.9414094090461732|38  |
|target_3_5 |970           |0.9776612520217896|40  |
|target_4_1 |960           |0.8500917851924896|26  |
|target_5_1 |999           |0.7375593483448029|9   |
|target_5_2 |790           |0.6967235207557678|4   |
|target_6_1 |560           |0.6979954838752747|5   |
|target_6_2 |999           |0.7185083627700806|6   |
|target_6_3 |905           |0.7512520551681519|13  |
|target_6_4 |815           |0.8511514961719513|27  |
|target_6_5 |975           |0.8954296708106995|31  |
|target_7_1 |999           |0.7979605495929718|19  |
|target_7_2 |999           |0.8309363126754761|24  |
|target_7_3 |999           |0.7614200413227081|14  |
|target_8_1 |999           |0.9749486446380616|39  |
|target_8_2 |999           |0.8348815143108368|25  |
|target_8_3 |999           |0.8577507436275482|28  |
|target_9_1 |975           |0.786454439163208 |16  |
|target_9_2 |999           |0.8191272020339966|22  |
|target_9_3 |999           |0.6842566132545471|3   |
|target_9_4 |975           |0.9044961929321288|33  |
|target_9_5 |675           |0.8254568874835968|23  |
|target_9_6 |999           |0.6833981573581696|2   |
|target_9_7 |999           |0.7478522658348083|12  |
|target_9_8 |995           |0.9168020486831664|36  |
|target_10_1|999           |0.7449418306350708|11  |


---------------------------

15.02.2026 

Экспресс-сравнение моделей (0007p.ipynb)
|tcol       |model                          |AUC   |model2                         |AUC2  |model3                         |AUC3  |
|-----------|-------------------------------|------|-------------------------------|------|-------------------------------|------|
|target_1_1 |Logistic Regression            |0.4957|Extra Trees Classifier         |0.4949|CatBoost Classifier            |0.4449|
|target_1_3 |Extra Trees Classifier         |0.9033|CatBoost Classifier            |0.8973|Random Forest Classifier       |0.8873|
|target_1_4 |Random Forest Classifier       |0.8118|Ridge Classifier               |0.7623|Extra Trees Classifier         |0.7431|
|target_2_1 |Extreme Gradient Boosting      |0.5449|Random Forest Classifier       |0.4862|CatBoost Classifier            |0.4855|
|target_2_2 |Extreme Gradient Boosting      |0.836 |CatBoost Classifier            |0.836 |Logistic Regression            |0.8066|
|target_2_4 |Extreme Gradient Boosting      |0.4696|Linear Discriminant Analysis   |0.4319|CatBoost Classifier            |0.4203|
|target_2_6 |Logistic Regression            |0.1957|Extreme Gradient Boosting      |0.1732|Random Forest Classifier       |0.1645|
|target_3_1 |Random Forest Classifier       |0.6272|Logistic Regression            |0.594 |CatBoost Classifier            |0.5823|
|target_3_2 |CatBoost Classifier            |0.8496|Random Forest Classifier       |0.8322|Gradient Boosting Classifier   |0.8269|
|target_3_3 |Ridge Classifier               |0.05  |Ada Boost Classifier           |0.05  |Linear Discriminant Analysis   |0.05  |
|target_3_4 |Ridge Classifier               |0.3696|Logistic Regression            |0.3565|Extreme Gradient Boosting      |0.3529|
|target_3_5 |Ridge Classifier               |0.05  |Ada Boost Classifier           |0.05  |Linear Discriminant Analysis   |0.05  |
|target_4_1 |Extra Trees Classifier         |0.2616|CatBoost Classifier            |0.2594|Quadratic Discriminant Analysis|0.2087|
|target_5_1 |Extreme Gradient Boosting      |0.4159|Quadratic Discriminant Analysis|0.3841|CatBoost Classifier            |0.3768|
|target_5_2 |Decision Tree Classifier       |0.2   |Dummy Classifier               |0.2   |K Neighbors Classifier         |0.1935|
|target_6_1 |Extreme Gradient Boosting      |0.2014|Dummy Classifier               |0.2   |K Neighbors Classifier         |0.1986|
|target_6_2 |Extra Trees Classifier         |0.3348|Random Forest Classifier       |0.3145|CatBoost Classifier            |0.3116|
|target_6_3 |CatBoost Classifier            |0.3928|Extra Trees Classifier         |0.3275|Extreme Gradient Boosting      |0.3232|
|target_6_4 |Light Gradient Boosting Machine|0.4667|Logistic Regression            |0.4493|Extra Trees Classifier         |0.4413|
|target_7_1 |Extreme Gradient Boosting      |0.6529|Light Gradient Boosting Machine|0.6367|Gradient Boosting Classifier   |0.6293|
|target_7_2 |Ada Boost Classifier           |0.6825|Light Gradient Boosting Machine|0.6228|CatBoost Classifier            |0.6167|
|target_7_3 |Ridge Classifier               |0.158 |Linear Discriminant Analysis   |0.1391|Naive Bayes                    |0.1   |
|target_8_1 |Random Forest Classifier       |0.9307|CatBoost Classifier            |0.9286|Extreme Gradient Boosting      |0.9284|
|target_8_2 |Random Forest Classifier       |0.6522|Extra Trees Classifier         |0.6514|CatBoost Classifier            |0.6352|
|target_8_3 |Random Forest Classifier       |0.7544|Ridge Classifier               |0.6727|Extreme Gradient Boosting      |0.6647|
|target_9_1 |Ridge Classifier               |0.2435|CatBoost Classifier            |0.2435|Naive Bayes                    |0.2304|
|target_9_2 |Light Gradient Boosting Machine|0.7705|CatBoost Classifier            |0.7346|Extra Trees Classifier         |0.7345|
|target_9_3 |SVM - Linear Kernel            |0.6969|Naive Bayes                    |0.6624|Quadratic Discriminant Analysis|0.6128|
|target_9_4 |Ridge Classifier               |0.05  |Ada Boost Classifier           |0.05  |Linear Discriminant Analysis   |0.05  |
|target_9_5 |Light Gradient Boosting Machine|0.3087|Ada Boost Classifier           |0.2986|Extreme Gradient Boosting      |0.2899|
|target_9_6 |Logistic Regression            |0.6408|CatBoost Classifier            |0.6244|Ridge Classifier               |0.6165|
|target_9_7 |Random Forest Classifier       |0.7342|CatBoost Classifier            |0.7293|Extra Trees Classifier         |0.7237|
|target_9_8 |Logistic Regression            |0.7891|Extra Trees Classifier         |0.786 |Random Forest Classifier       |0.7628|
|target_10_1|Gradient Boosting Classifier   |0.732 |CatBoost Classifier            |0.7173|Extra Trees Classifier         |0.6945|
