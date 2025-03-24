# Metro Simulation

GAIH Bootcamp Projesi

Bu projede bir metro ağı üzerinde iki farklı algoritma kullanılarak rota optimizasyonu yapılmıştır:

- **En az aktarmalı rota** (BFS algoritması ile)
- **En hızlı rota** (A* algoritması ile)

Amacımız, metro ağındaki rota optimizasyonunu algoritmik yaklaşımlarla çözmektir.

## Kullanılan Algoritmalar

### 1. BFS Algoritması (En Az Aktarma)

- **Amaç:**  
  İki istasyon arasındaki en az aktarmalı (yani en az düğüm geçişi) rotayı bulmak.

- **Çalışma Prensibi:**  
  - Komşu istasyonlar, Breadth-First Search (BFS) yöntemiyle, genişlik öncelikli olarak keşfedilir.  
  - Ziyaret edilen istasyonlar takip edilerek, en az aktarma içeren kısa yol elde edilir.

- **Kullanılan Yapılar:**  
  - `deque` ile kuyruk yapısı  
  - `set` ile ziyaret edilen istasyonlar takibi  

---

### 2. A* Algoritması (En Hızlı Rota)

- **Amaç:**  
  Toplam seyahat süresini minimize ederek en hızlı rotayı bulmak.

- **Çalışma Prensibi:**  
  - Her adımda toplam süre hesaplanarak, A* algoritması yardımıyla en düşük maliyetli rota önceliklendirilmektedir.  
  - `heapq` modülü ile oluşturulan öncelik kuyruğunda, en uygun rota seçilir.

- **Kullanılan Yapılar:**  
  - `heapq` ile öncelik kuyruğu  
  - `set` ile ziyaret edilen istasyonlar takibi  

## Neden Bu Algoritmalar Tercih Edildi?

- Metro ağı, her bir istasyonu bir düğüm ve istasyonlar arasındaki bağlantıları bir kenar olarak modellediğinden, **BFS algoritması** ile en az aktarma sayısını elde etmek doğrudan probleme uygundur.
- **A\* algoritması**, seyahat süresi gibi maliyet ölçütlerini göz önüne alarak, en hızlı yolu hesaplamak için ideal bir seçimdir.
