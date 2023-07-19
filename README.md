# python-sayi_tahmin_oyunu
import random

def sayi_tahmin_oyunu():
    print("Sayı Tahmin Oyununa Hoş Geldiniz!")
    rastgele_sayi = random.randint(1, 100)  # 1 ile 100 arasında rastgele bir sayı seçiyoruz
    tahmin_hakki = 5

    while tahmin_hakki > 0:
        tahmin = int(input("Tahmininizi girin (1-100 arasında): "))

        if tahmin == rastgele_sayi:
            print("Tebrikler! Doğru tahmin ettiniz.")
            break
        elif tahmin < rastgele_sayi:
            print("Daha yüksek bir sayı tahmin edin.")
        else:
            print("Daha düşük bir sayı tahmin edin.")

        tahmin_hakki -= 1

    if tahmin_hakki == 0:
        print("Tahmin hakkınız bitti. Rastgele sayı:", rastgele_sayi)

sayi_tahmin_oyunu()
