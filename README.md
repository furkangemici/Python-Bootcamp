# 🚆 Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

Bu proje, bir metro ağı içinde en hızlı ve en az aktarmalı rotayı bulan bir simülasyon içerir.  
Breadth-First Search (**BFS**) ve **A* (A-Star) algoritmaları** kullanılarak en iyi rota hesaplanır.

## 📌 Proje Özellikleri
- **En az aktarma rotasını bulma** (BFS algoritması)
- **En hızlı rotayı bulma** (A* algoritması)
- **Gerçekçi metro ağı modelleme**
- **Farklı metro hatları ve istasyon bağlantıları**

## 🚀 Kullanılan Teknolojiler & Kütüphaneler
- Python 3
- `collections.deque` → **BFS için kuyruk yapısı**
- `heapq` → **A* için öncelikli kuyruk yapısı**
- `typing` → **Tip tanımlamaları**

## 🧠 Algoritmaların Çalışma Mantığı
### **1️⃣ BFS (Breadth-First Search)**
BFS, **katman katman arama yaparak** en az aktarma ile ulaşılacak rotayı belirler.
- **Ziyaret edilen istasyonlar takip edilir.**
- **Komşu istasyonlar sırasıyla kuyruğa eklenir.**
- **En az aktarma ile hedefe ulaşan yol döndürülür.**

### **2️⃣ A* (A-Star) Algoritması**
A* algoritması, **öncelikli kuyruk (heapq) kullanarak en hızlı rotayı bulur.**
- **Toplam süre hesaplanır ve en kısa sürede gidilecek yol seçilir.**
- **Öncelik kuyruğundaki en düşük maliyetli rota her adımda seçilir.**

## 🔍 Örnek Kullanım & Test Sonuçları
```bash
=== Test Senaryoları ===

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ → Kızılay → Kızılay → Ulus → Demetevler → OSB
En hızlı rota (25 dakika): AŞTİ → Kızılay → Kızılay → Ulus → Demetevler → OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent → Demetevler → Gar → Keçiören
En hızlı rota (21 dakika): Batıkent → Demetevler → Gar → Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören → Gar → Gar → Sıhhiye → Kızılay → AŞTİ
En hızlı rota (19 dakika): Keçiören → Gar → Gar → Sıhhiye → Kızılay → AŞTİ
