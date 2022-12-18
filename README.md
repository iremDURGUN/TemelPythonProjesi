# TemelPythonProjesi
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. <br/>
Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak: <br/>

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5] <br/>

output: [1,'a','cat',2,3,'dog',4,5] <br/>

--

<p> dizi = [[1,'a',['cat'],2],[[[3]],'dog'],4,5] &nbsp;&nbsp;&nbsp; #Diziyi tanımlarız. <br/></p>
<p>atanacakDizi = []    &nbsp;&nbsp;&nbsp;   #İşlem yaptıktan sonra atama yaoılması için boş bir dizi tanımlarız. <br/><p>

<p>def flatten(k):    &nbsp;&nbsp;&nbsp;    #flatten diye bir fonksiyon oluşturuyoruz. <br/><p>
<p>  &nbsp;&nbsp;for i in k :     &nbsp;&nbsp;&nbsp;  #fonksiyonun içinde gezinmek için bir for dögüsü oluşturuyoruz. <br/><p>
<p>  &nbsp;&nbsp;    if isinstance(i,list):   &nbsp;&nbsp;&nbsp;  #i değişkeni listede mi? <br/><p>
<p>  &nbsp;&nbsp;   flatten(i)   &nbsp;&nbsp;&nbsp;      #i değişkeni düzleştirilir. <br/>
        else:                                        
<p>  &nbsp;&nbsp;   atanacakDizi.append(i)  &nbsp;&nbsp;&nbsp;  #i listede değilse oluşturulan boş diziye i değişkeni atanacak. <br/>

<p>  &nbsp;&nbsp; flatten(dizi)   &nbsp;&nbsp;&nbsp;    #latten fonksiyonu çalıştırılır. <br/>
<p> &nbsp;&nbsp; print(atanacakDizi)   &nbsp;&nbsp;&nbsp;   #atanacakDizi ekrana yazdırılır. <br/> 
 



2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. <br/>
Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak: <br/>

input: [[1, 2], [3, 4], [5, 6, 7]] <br/>

output: [[[7, 6, 5], [4, 3], [2, 1]] <br/>

--

<p> &nbsp;&nbsp; dizi = [[1, 2], [3, 4], [5, 6, 7]] &nbsp;&nbsp;&nbsp;        #İşlem yapılacak dizi tanımlanır. <br/>
<p> &nbsp;&nbsp; dizi.reverse()         &nbsp;&nbsp;&nbsp;                    #Diziyi reverse fonksiyonu kullanılarak ters çeviririz. <br/>

<p> &nbsp;&nbsp; for i in range(len(dizi)):    &nbsp;&nbsp;&nbsp;        #Dizinin içinde eleman uzunluğu kadar döneriz bunun tespitini len fonksiyonuyla yaparız. <br/>
<p> &nbsp;&nbsp;&nbsp;    (dizi[i])=(dizi[i])[::-1]     &nbsp;&nbsp;&nbsp;         #Dilimleme yaparak dizinin içindeki dizilerinde ters dönmesini sağlarız.  <br/>

<p> &nbsp;&nbsp; print(dizi)             &nbsp;&nbsp;&nbsp;                   #Ters çevirdiğimiz dizyi ekrana yazdırırız.
