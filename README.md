# TemelPythonProjesi
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. <br/>
Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak: <br/>

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5] <br/>

output: [1,'a','cat',2,3,'dog',4,5] <br/>

--

dizi = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]             #Diziyi tanımlarız. <br/>
atanacakDizi = []                                        #İşlem yaptıktan sonra atama yaoılması için boş bir dizi tanımlarız. <br/>

def flatten(k):                                          #flatten diye bir fonksiyon oluşturuyoruz. <br/>
    for i in k :                                         #fonksiyonun içinde gezinmek için bir for dögüsü oluşturuyoruz. <br/>
        if isinstance(i,list):                           #i değişkeni listede mi? <br/>
            flatten(i)                                   #i değişkeni düzleştirilir. <br/>
        else:                                        
            atanacakDizi.append(i)                       #i listede değilse oluşturulan boş diziye i değişkeni atanacak. <br/>

flatten(dizi)                                            #latten fonksiyonu çalıştırılır. <br/>
print(atanacakDizi)                                      #atanacakDizi ekrana yazdırılır. <br/>
 



2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. <br/>
Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak: <br/>

input: [[1, 2], [3, 4], [5, 6, 7]] <br/>

output: [[[7, 6, 5], [4, 3], [2, 1]] <br/>

--

dizi = [[1, 2], [3, 4], [5, 6, 7]]         #İşlem yapılacak dizi tanımlanır. <br/>
dizi.reverse()                             #Diziyi reverse fonksiyonu kullanılarak ters çeviririz. <br/>

for i in range(len(dizi)):                 #Dizinin içinde eleman uzunluğu kadar döneriz bunun tespitini len fonksiyonuyla yaparız. <br/>
    (dizi[i])=(dizi[i])[::-1]              #Dilimleme yaparak dizinin içindeki dizilerinde ters dönmesini sağlarız.  <br/>

print(dizi)                                #Ters çevirdiğimiz dizyi ekrana yazdırırız.
