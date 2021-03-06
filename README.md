# Gogus-Kafesi-Tespit-Programi
Röntgen filminden akciğer kısmını kırpan, yapay zeka destekli zatürre teşhis projesinin veriseti hazırlama (preprocessing) uygulaması.

Algoritmaya verilen röntgen filmi:![d](https://user-images.githubusercontent.com/58745898/158307662-107506fb-edaa-4460-bc8d-b9fd581bce2e.jpg)

Çalışma adımları kısa ve özetle şu şekildedir:

1.İlk olarak yüksek bir eşik değeri ile film siyah beyaz hale getirilerek, yazı ve semboller tespit edilir.
![a](https://user-images.githubusercontent.com/58745898/158308128-d75a6b0e-536c-48ed-8690-fb02222c4288.jpg)
2.Tespit edilen yazı ve sembollerin filmdeki koordinatları siyaha boyanır.
![a](https://user-images.githubusercontent.com/58745898/158308404-fbe4cac4-c006-4db4-af32-628e9971674e.jpg)
3.Filme blur uygulanır.
![a](https://user-images.githubusercontent.com/58745898/158308657-f52d49fd-6e06-45f0-a16f-e539cd3440af.jpg)
4.Blurlanmış film siyah beyaz hale getirilir.
![a](https://user-images.githubusercontent.com/58745898/158308790-7b0e7d41-12b5-478f-aeca-6fb68fba7d00.jpg)
5.Filmin en sol, en sağ, en üst ve en altında bulunan beyaz pixeller tespit edilerek, vücudun çerçevesi belirlenir. 4. maddede işlenmiş olan görüntü bu çerçevelerden kırpılarak akciğer bulma fonksiyonuna gönderilir.
![Adsız](https://user-images.githubusercontent.com/58745898/158309814-01622bc7-a118-4b30-83a1-a8c72a78d91b.png)
6.Filmin dışta bulunan tüm siyah pixelleri beyaza boyanır.
![a](https://user-images.githubusercontent.com/58745898/158310148-6b933059-2b21-450f-8af2-fcaba122d0da.jpg)
7.Elde edilen görüntü blurlanır.
![a](https://user-images.githubusercontent.com/58745898/158310363-6233b803-7aee-4451-95af-0bf714084bb9.jpg)
8.Blurlanmış görüntü siyah beyaza çevirilerek göğüs kafesi ortaya çıkarılır.
![a](https://user-images.githubusercontent.com/58745898/158310655-a8acfd73-15fc-4f3d-a1f7-13bf40d1c119.jpg)
9.Görüntünün en sol, en sağ, en üst ve en altında bulunan siyah pixeller tespit edilerek, göğüs kafesinin çerçevesi belirlenir.
![a](https://user-images.githubusercontent.com/58745898/158311151-279416cb-d603-4041-bdcb-192be0719e2f.jpg)
10.Orijinal görüntü bu çerçevelerden kesilerek istenilen görüntüye ulaşılır.
![a](https://user-images.githubusercontent.com/58745898/158311599-b0303496-4b32-46e7-ac5a-103e81cd8721.jpg)
11.Elde edilen görüntü:
![d-9079045](https://user-images.githubusercontent.com/58745898/158310672-3c56a853-088f-4295-a238-c712b75ca318.jpg)
