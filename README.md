
# VERİ SETİ ETİKETLEMESİ

## Kurulum

Veri setini etiketlemek için ilk olarak Drive'daki veri setini indirmek gerekir. İndirilen veri setini bir dizin içerisinde başka bir dizine kaydedin. Örneğin:

```bash
    -dataset
    - -traffic_sign_dataset
    - - -katot_0.jpg
    - - -katot_1.jpg
    - - -...
```
Şeklinde olsun. Sonrasında dataset dizini içerisinde bu depoyu klonlayın.

```bash
    git clone https://github.com/Albaryan/labels.git
```

Sonucunda dizinlerin şu şekilde olması gerekir:
```bash
    -dataset/
    - -traffic_sign_dataset/
    - - -katot_0.jpg
    - - -katot_1.jpg
    - - -...
    - -labels/
    - - -dataset_labels/
    - - - -classes.txt
    - - - -katot_0.txt
    - - - -katot_1.txt
    - - - -...
```

## Etiketleme

Etiketlemeye başlamadan önce GitHub'a yüklenmiş olan güncellemelerin çekilmesi gerekir. Bunun için labels dizininin içerisine girerek aşağıdaki kodu yazın. Bunu etiketlemeye başlamadan önce her seferinde yapmanız gerekir.

```bash
    git pull
```

Etiketleme için labelImg kullanılacağı için programının kurulu olduğundan emin olun. Sonrasında traffic_sign_dataset dizini içerisinde aşağıdaki kodu çalıştırın.

```bash
    labelImg . ../labels/dataset_labels/classes.txt
```

Bu kodu çalıştırdıktan sonra labelImg'in açılması gerekir. Sonrasında sol panelde bulunan "change save dir"e basın. /labels/dataset_labels dizinini seçerek open deyin. Sonrasında labelImg'i kapatıp aşağıdaki kodu çalıştırın.

```bash
    labelImg . ../labels/dataset_labels/classes.txt
```

Program açıldığında veri etiketlenmiş olan veri setlerinin görülebiliyor olması gerekir. Bundan sonraki aşamada etiketleme işlemini yapabilirsiniz. labelImg programını açarken kullanılan kodda classes.txt dosyası seçildiğinden dolayı her etiketleme yaptığınızda karşınıza önceden tanımlanmış sınıf adlarının gelmesi gerekir.

Etiketleme yaparken sadece etiketleme değil aynı zamanda kontrol de yapmanız gerekir. Önceden yapılan etiketlerin sınıf adları farklı olacaktır. Onları doğru sınıf adları ile eşleştirmeniz gerekir. Öncelik Teknofest olmasından dolayı şartnamede bulunmayan tabelaları etiketlemeyin. Etiketliyse de etiketini silebilirsiniz. Aynı fotoğrafta hem şartnamede bulunan hem de bulunmayan fotoğraflar bulunabilir. Şartnamede bulunanları düzenleyerek/etiketleyerek devam edebilirsiniz.

## Yükleme

Etiketleme işlemleri tamamlandıktan sonra kodun GitHub'daki depoya yüklenmesi gerekir. Bunun işin labels dizini içerisine girip aşağıdaki kodları yazın.

```bash
    git add .
    git commit -m "Buraya etiketlediğiniz aralığı girin. Örneğin : 500-600"
    git push origin master
```

Sonrasında README.md dosyasını açarak en altta kalan tabloyu kaldığınız yere göre doldurun. 

(labelImg'i açtığınızda en üstte verinin kaçıncı veri olduğunun sayısı) - (verinin adı)


| Sorumlular |   Alper Tuna  | Ömer Berat Yıldırım | Ömer Çavdar | Ayberk Sungurtaş |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Sorumlu olduğu yer  | 0-3999  | 4000-7999  | 8000-11999  | 12000-15999 |
| Kaldığı yer | Bitirildi | Başlanacak  | 10000 | Başlanacak |
