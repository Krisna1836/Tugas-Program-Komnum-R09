# Tugas-Program-Komnum-R09

## Fungsi f(x)
def F(x):
    return x**3 + 6 * x**2 - 19*x - 84
### ini adalah fungsi polinomial derajat tiga.

## Fungsi df(x)
def Df(x):
    return 3 * x**2 + 12*x - 19
### Fungsi df(x) adalah fungsi turunan dari f(x). Ini untuk mencari gradien ataupun titik eksrem(minimum dan maximum).

## Fungsi Flounder(x)
def Flounder(x):
    if ((x*1000) % 10 >= 5):
        return (((x*100) - ((x*100) % 1)) / 100 + 0.01)
    else:
        return (((x*100) - ((x*100) % 1)) / 100)
### Fungsi ini membulatkan 2 angka dibelakang koma namun manual. Cara kerjanya dikalikan dengan 1000(untuk melihat 3 angka belakang koma), jika angka >= 5 bulatkan ke atas, < 5 bulatkan ke bawah

## Algoritma Newton Raphson
1. Inisialisasi x = -4 (nilai tebakan awal). Nilai akar sebenarnya adalah xt = -3
2. Lakukan iterasi Newton-Raphson: x = x - F(x) / Df(x)
3. Tampilkan hasil: print("Iterasi ke -", i, ":\nTanpa pembulatan: ", x, "\nDengan pembulatan: ", Flounder(x), "\n") i += 1
4. Algoritma akan terus berjalan hingga x===xt x mungkin tidak pernah tepat sama dengan xt. Untuk penggunaan nyata, sebaiknya gunakan batas toleransi, seperti:
while abs(x - xt) > 1e-6:

