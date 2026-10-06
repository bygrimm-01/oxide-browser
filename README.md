# Oxide Browser

Windows için Firefox ESR tabanlı tarayıcı projesi. Henüz derlenmiş tarayıcı yoktur.

## Aşama 1: ücretsiz derleme ortamını ölçme

`.github/workflows/runner-check.yml`, GitHub Actions üzerinde standart
`ubuntu-24.04` ve `windows-2022` makinelerinin işlemci, bellek, boş disk ve
araç bilgilerini raporlar. Linux üzerinde seçili hazır araç klasörlerinin
boyutlarını da ölçer. Dosya silmez ve kaynak kodu indirmez.

### Çalıştırma

1. Dosyayı herkese açık GitHub deposunun varsayılan dalına ekle.
2. **Actions → Oxide - Runner Check → Run workflow** seç.
3. İki iş tamamlandığında her işin özetindeki boş disk ve RAM değerlerini incele.

Yeşil sonuç yalnızca ölçümün tamamlandığını belirtir. Firefox derlemesinin
sığacağı veya başarıyla tamamlanacağı henüz doğrulanmış değildir.
Kırmızı sonuçta hata veren adımın günlüğüne bak; iş 10 dakika sınırına
takıldıysa bunun derleme hatası olmadığını unutma. Henüz derleme yapılmaz.

Bu kontrol yerel bilgisayara MozillaBuild veya Firefox kaynaklarını kurmaz.
Manuel başlatılır; otomatik tekrar, cache veya artifact yüklemesi içermez.

## Kaynaklar

- [GitHub standart makineleri](https://docs.github.com/en/actions/reference/runners/github-hosted-runners)
- [GitHub Actions sınırları](https://docs.github.com/en/actions/reference/limits)
- [Mozilla Windows derleme rehberi](https://firefox-source-docs.mozilla.org/setup/windows_build.html)

Firefox kaynakları eklendiğinde mevcut MPL 2.0 bildirimleri korunacaktır.
