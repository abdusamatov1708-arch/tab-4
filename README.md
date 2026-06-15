# tab-4
# ==============================================================================
# DASTUR TAVSIFI:
# Ushbu dastur foydalanuvchi kiritgan matn ustida mukammal tahlil o'tkazadi.
# Dasturda kamida 5 ta string metodi (strip, split, lower, upper, replace),
# matn uzunligi, so'zlar soni, slicing hamda f-string formatlash qo'llanilgan.
# Shuningdek, bo'sh matn kiritilgan holat ham alohida nazoratga olingan.
# ==============================================================================

print("=" * 60)
print("                     MATN TAHLILCHISI                           ")
print("=" * 60)

# Foydalanuvchidan matn qabul qilish va boshidagi/oxiridagi bo'shliqlarni o'chirish
# 1-metod: .strip()
foydalanuvchi_matni = input("Tahlil qilish uchun matn kiriting:\n> ").strip()

print("\n" + "-" * 60)
print("                     TAHLIL NATIJALARI                          ")
print("-" * 60)

# 1. Bo'sh matn holatini tekshirish
if not foydalanuvchi_matni:
    print("❌ Xatolik: Siz hech qanday matn kiritmadingiz!")
else:
    # 2. String metodlari yordamida matnni qayta ishlash
    # 2-metod: .split() — matnni so'zlarga ajratadi
    sozlar_royxati = foydalanuvchi_matni.split()
    sozlar_soni = len(sozlar_royxati)
    
    # Matn uzunligi (belgilar soni)
    belgilar_soni = len(foydalanuvchi_matni)
    
    # 3-metod: .lower() — unli/undoshlarni sanash uchun matnni kichik harfga o'tkazamiz
    kichik_matn = foydalanuvchi_matni.lower()
    
    # Unli va undosh harflarni hisoblash
    unlilar_ombori = "aeiouo'o‘g'g‘"  # O'zbek tilidagi unli harflar
    unlilar_soni = sum(1 for harf in kichik_matn if harf in unlilar_ombori and harf.isalpha())
