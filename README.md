# animal_classifier
A project to recognize animals using deep learning.
animal-recognition
A project to recognize animals using deep learning

Hayvan Görüntü Sınıflandırma Uygulaması
Bu proje, PyTorch ve Gradio kullanılarak geliştirilmiş bir görüntü sınıflandırma uygulamasıdır. Uygulama, kullanıcı tarafından yüklenen bir görseli analiz ederek yalnızca hayvan kategorilerine ait sınıfları tespit eder. Görseller, önceden ImageNet veri seti ile eğitilmiş ResNet50 modeli kullanılarak sınıflandırılır. Sonuç olarak en yüksek olasılığa sahip ilk beş sınıf arasından yalnızca hayvanlara ait olanlar kullanıcıya sunulur.

Özellikler
PyTorch üzerinden ResNet50 önceden eğitilmiş model ile sınıflandırma
Görüntüleri otomatik olarak yeniden boyutlandırma ve normalize etme
İlk 5 sınıf tahmini içerisinden yalnızca hayvan sınıflarının filtrelenmesi
Gradio ile kullanıcı dostu web arayüzü
Tek tıklamayla sınıflandırma işlemi başlatma
Kullanılan Teknolojiler
Python
PyTorch
Torchvision
Gradio
PIL (Pillow)
Requests (ImageNet etiketlerini çekmek için)
Kurulum
Python 3.x kurulu olduğundan emin olun.
Aşağıdaki komut ile gerekli kütüphaneleri yükleyin: pip install torch torchvision gradio pillow requests
Uygulamayı çalıştırmak için terminalde aşağıdaki komutu kullanın:python app.py
Kullanım
Uygulama çalıştırıldığında Gradio üzerinden yerel bir arayüz başlatılır. Arayüzde:

Bir görsel yüklenir.
“Sınıflandır” butonuna tıklanır.
En yüksek olasılıkla tahmin edilen hayvan sınıfı ve diğer olası hayvan sınıfları görüntülenir.
Eğer görsel hayvan içermiyorsa, kullanıcıya hayvan sınıfı bulunamadığına dair bir bilgi mesajı sunulur.

Teknik Detaylar
Görsel, transforms.Resize, transforms.CenterCrop, transforms.ToTensor ve transforms.Normalize adımları ile ön işlenir.
Model torch.no_grad() bloğu içinde çalıştırılır ve softmax ile olasılıklar hesaplanır.
İlk 5 sınıf torch.topk ile seçilir.
Hayvan sınıfları belirli anahtar kelimeler (dog, cat, bird, horse, vs.) kullanılarak filtrelenir.
Gradio arayüzünde görsel giriş, sınıflandırma butonu ve sonuç metin kutuları yer alır.
# animal-recognition
A project to recognize animals using deep learning
# Hayvan Görüntü Sınıflandırma Uygulaması

Bu proje, PyTorch ve Gradio kullanılarak geliştirilmiş bir görüntü sınıflandırma uygulamasıdır. Uygulama, kullanıcı tarafından yüklenen bir görseli analiz ederek yalnızca hayvan kategorilerine ait sınıfları tespit eder. Görseller, önceden ImageNet veri seti ile eğitilmiş ResNet50 modeli kullanılarak sınıflandırılır. Sonuç olarak en yüksek olasılığa sahip ilk beş sınıf arasından yalnızca hayvanlara ait olanlar kullanıcıya sunulur.

## Özellikler

- PyTorch üzerinden ResNet50 önceden eğitilmiş model ile sınıflandırma
- Görüntüleri otomatik olarak yeniden boyutlandırma ve normalize etme
- İlk 5 sınıf tahmini içerisinden yalnızca hayvan sınıflarının filtrelenmesi
- Gradio ile kullanıcı dostu web arayüzü
- Tek tıklamayla sınıflandırma işlemi başlatma

## Kullanılan Teknolojiler

- Python
- PyTorch
- Torchvision
- Gradio
- PIL (Pillow)
- Requests (ImageNet etiketlerini çekmek için)

## Kurulum

1. Python 3.x kurulu olduğundan emin olun.
2. Aşağıdaki komut ile gerekli kütüphaneleri yükleyin: pip install torch torchvision gradio pillow requests
3. Uygulamayı çalıştırmak için terminalde aşağıdaki komutu kullanın:python app.py


## Kullanım

Uygulama çalıştırıldığında Gradio üzerinden yerel bir arayüz başlatılır. Arayüzde:

- Bir görsel yüklenir.
- “Sınıflandır” butonuna tıklanır.
- En yüksek olasılıkla tahmin edilen hayvan sınıfı ve diğer olası hayvan sınıfları görüntülenir.

Eğer görsel hayvan içermiyorsa, kullanıcıya hayvan sınıfı bulunamadığına dair bir bilgi mesajı sunulur.

## Teknik Detaylar

- Görsel, `transforms.Resize`, `transforms.CenterCrop`, `transforms.ToTensor` ve `transforms.Normalize` adımları ile ön işlenir.
- Model `torch.no_grad()` bloğu içinde çalıştırılır ve softmax ile olasılıklar hesaplanır.
- İlk 5 sınıf `torch.topk` ile seçilir.
- Hayvan sınıfları belirli anahtar kelimeler (dog, cat, bird, horse, vs.) kullanılarak filtrelenir.
- Gradio arayüzünde görsel giriş, sınıflandırma butonu ve sonuç metin kutuları yer alır.
