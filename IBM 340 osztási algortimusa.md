---
tags: OE/ALKMAT/Mernoki1 
aliases:
---
# IBM 340 osztási algoritmusa
1.  Normalizáció: A bemeneti számot a lehető legnagyobb számjegy számára normalizálta, hogy nagyobb legyen az osztóval való osztás hatékonysága.
2.  Osztócsökkentés: Az osztót az előbbi normalizáció után a lehető legkisebb számra csökkentette, amely osztóval az eredeti osztás egyenértékű volt.
3.  Szorzás és kivonás: A normalizált bemeneti számot és az osztót szorozta, majd kivonta az eredményt a normalizált bemeneti számból. Ezután ezt a lépést megismételte az előbbi eredménnyel és az osztóval, amíg az eredmény nulla vagy kisebb lett.
4.  Hátralék: Az előző lépésben kapott maradékkal elvégezte az osztást, és ez volt az eredmény.
#chatGPT 