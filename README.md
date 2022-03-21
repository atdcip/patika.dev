# patika.dev
[22, 27, 16, 2, 18, 6] Algoritmamız her seerinde ileri doğru giderek, dizinin elemanını, geride kalan elemanlarla kıyaslayarak tek tek kıyaslar ve küçükse yer değiştirir. 22'den başlayıp tek tek kıyaslama yapar.

Adım-> 22| 27 16 2 18 6 -> İlk geçişte 22 sayısı sıralıdır ve hiçbir işlem yapmadan devam eder.

Adım-> 22 27| 16 2 18 6 -> İkinci geçişte 27 ve 22 sayısı kıyaslanır. 22, 27'den küçüktür. Değişiklik olmaz.

Adım-> 22 27 16| 2 18 6 -> Üçüncü geçişte 16 ve 27 kıyaslanır. 16, 27'den küçüktür. 16 ve 27'yi yer değiştirir.(swap) Sonra tekrar 16 ve 22'yi kıyaslar. 16, 22'den küçüktir. 16 ve 22 nin yerini değiştirir.

22 27 16| 2 18 6 -> 22 16 27| 2 18 6 -> 16 22 27| 2 18 6

Adım-> 16 22 27 2| 18 6 -> 16 22 2 27| 18 6 -> 16 2 22 27| 18 6 -> 2 16 22 27| 18 6

Adım-> 2 16 22 27 18| 6 -> 2 16 22 18 27| 6 -> 2 16 18 22 27| 6

Adım-> 2 16 18 22 27 6| -> 2 16 18 22 6 27| -> 2 16 18 6 22 27| -> 2 16 6 18 22 27| -> 2 6 16 18 22 27|

Bu şekilde dizimiz sıralı hale gelir. Son hali; [2, 6, 16, 18, 22, 27]

11 işlem yapıldı.

2)Big-O gösterimini yazınız.

O(n^2)

3)Time Complexity:

Average Case: Aradığımız sayının ortada olması -> O(n^2) Worst Case: Aradığımız sayının sonda olması -> O(n^2) Best Case: Aradığımız sayının dizinin en başında olması -> O(n)

Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.
Sıralı dizimiz-> [2, 6, 16, 18, 22, 27] Average case kapsamına girer.

2. Örnek
[7, 3, 5, 8, 2, 9, 4, 15, 6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

7| 3 5 8 2 9 4 15 6

7 3| 5 8 2 9 4 15 6 -> 3 ve 7 yer değiştirir.

3 7 5| 8 2 9 4 15 6 -> 5 ve 7 yer değiştirir.

3 5 7| 8 2 9 4 15 6

3 5 7 8| 2 9 4 15 6 -> geride kalan sayılardan büyük olduğu için işlem yapılmaz.

3 5 7 8 2| 9 4 15 6 -> 3 5 7 2 8| 9 4 15 6 -> 3 5 2 7 8| 9 4 15 6 -> 3 2 5 7 8| 9 4 15 6 -> 2 3 5 7 8| 9 4 15 6

adımdan sonraki hali; [2, 3, 5, 7, 8| 9, 4, 15, 6]
