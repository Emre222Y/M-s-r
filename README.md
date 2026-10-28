# Mısırda Büyüme Derece-Gün ile Hasat Tarihi Tahmini

Günlük ortalama sıcaklık verisinden büyüme derece-gün (GDD) yöntemiyle
mısırın hasat olgunluğuna ulaşacağı tarihi hesapladım.

## Parametreler
- Hasat olgunluğu: 1330 derece-gün
- Alt eşik sıcaklık: 10 °C, üst eşik sıcaklık: 38 °C
- Ekim tarihi: 10 Nisan
- Veri: Mart-Ekim günlük ortalama sıcaklıklar (°C)

## Yöntem
1. Günlük derece-gün: `MAX(0; MIN(T; 38) - 10)`
2. Nisan (10'undan itibaren) - Temmuz toplamı: 1119
3. Ağustos'ta günlük birikimli toplam alındı
4. Toplamın 1330'u ilk geçtiği gün hasat tarihi

## Sonuç
17 Ağustos'ta birikimli 1326, 18 Ağustos'ta 1340 → **Hasat olgunluğu: 18 Ağustos**

## Öğrendiklerim
- Boş bir hücre `MIN` formülünde yanlış değer (28) üretip toplamı bozdu
- Aylık toplamları kontrol değerleriyle doğrulayarak hataları buldum

Araç: WPS Spreadsheets / Excel
