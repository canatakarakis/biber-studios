# biber-studios

Biber Studios kurucu ortak ve yonetim kurulu plugin'i.

## Bilgi mimarisi

Bu repo **davranis** tasir: skill ve agent'larin nasil dusunecegi.
**Bilgi** burada degil — claude.ai projesindeki `biber/*.md` belgelerinde:
rol, yetki siniri, marka cekirdegi, cerceveler, sablonlar.

Bir kurali degistirmek icin bu repoya dokunma; ilgili proje belgesini
duzenle. Yetki sinirini degistirmek icin: `biber/co-ceo-cekirdek.md` bolum 3.

## Bilesenler

| Bilesen | Tip | Ne yapar |
|---|---|---|
| `co-ceo` | skill | Kurucu ortak / dusunme ortagi. Itiraz eder, secenek uretir, karari Can'a birakir |
| `koleksiyon-brief` | skill | Koleksiyon ve urun brief'i. Cikti tedarik aramasi icin: Ingilizce arama terimleri, MOQ, maliyet araligi, eleme kriterleri |
| `rakip-tarama` | agent | Rakip taramasi ve RACE karsilastirmasi. Ayri baglamda calisir |

## Tasarim kurali

- **Skill** = ana sohbette, Can'a soru sorabilen is
- **Agent** = ayri baglamda, girdisi ve ciktisi net olan is
- Agent'lar unvan seklinde degil (CFO, CMO), **is seklinde** tanimlanir
- Her bilesen once `biber/co-ceo-cekirdek.md`'yi okur

## Sonraki adimlar

- Gun basi / hafta brief'i
- Aci-Tatli ses denetimi
- Tedarik tarama agent'i
- Rol gozlukleri (finans, pazarlama, operasyon) — agent degil, skill olarak
- Agent'lara `tools` kisiti (ilk testten sonra, hangi araclara ihtiyac
  duyduklari netlesince)

## Kurulum

Bu repo kendi marketplace'ini tasir. Claude'da:
`/plugin marketplace add canatakarakis/biber-studios`
sonra `biber-studios` plugin'ini kur.
