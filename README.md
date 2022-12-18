# TemelPythonProjesi
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. 
Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]

--

dizi = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]         #Diziyi tanımlarız.
atanacakDizi = []                                    #İşlem yaptıktan sonra atama yaoılması için boş bir dizi tanımlarız.

def flatten(k):                                      #flatten diye bir fonksiyon oluşturuyoruz.
    for i in k :                                     #fonksiyonun içinde gezinmek için bir for dögüsü oluşturuyoruz.
        if isinstance(i,list):                       #i değişkeni listede mi?
            flatten(i)                               #i değişkeni düzleştirilir.
        else:                                        
            atanacakDizi.append(i)                   #i listede değilse oluşturulan boş diziye i değişkeni atanacak.

flatten(dizi)                                        #latten fonksiyonu çalıştırılır.
print(atanacakDizi)                                 #atanacakDizi ekrana yazdırılır.
 



2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın.
Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]

--

dizi = [[1, 2], [3, 4], [5, 6, 7]]     #İşlem yapılacak dizi tanımlanır.
dizi.reverse()                         #Diziyi reverse fonksiyonu kullanılarak ters çeviririz.

for i in range(len(dizi)):             #Dizinin içinde eleman uzunluğu kadar döneriz bunun tespitini len fonksiyonuyla yaparız.
    (dizi[i])=(dizi[i])[::-1]          #Dilimleme yaparak dizinin içindeki dizilerinde ters dönmesini sağlarız. 

print(dizi)                            #Ters çevirdiğimiz dizyi ekrana yazdırırız.
