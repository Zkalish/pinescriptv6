---
name: Pine Script v6
description: TradingView Pine Script v6 programlama dili uzmanlığı
version: 1.0
author: Pine Script Community
tags: [pinescript, tradingview, trading, indicators, strategies]
---

# Pine Script v6 Skill

> TradingView Pine Script v6 programlama dili uzmanlığı

## Açıklama

Bu skill, TradingView Pine Script v6 dokümantasyonunu içerir. Pine Script, TradingView platformunda teknik analiz araçları ve otomatik ticaret stratejileri geliştirmek için kullanılan programlama dilidir.

## Temel Kurallar

1. Tüm kodlar `//@version=6` ile başlamalıdır
2. Fonksiyonlar için `ta.*`, `strategy.*`, `request.*` namespace'lerini kullan
3. Görselleştirme için `plot`, `line`, `box`, `label` fonksiyonlarını kullan
4. Backtesting için `strategy.entry`, `strategy.exit` kullan

## Dosya Yapısı

- **LLM_MANIFEST.md**: Ana rehber - başlangıç noktası
- **concepts/**: Kavramlar ve açıklamalar
  - execution_model.md: Bar-by-bar çalışma modeli
  - timeframes.md: Multi-timeframe veri işleme
  - colors_and_display.md: Renk ve görüntüleme
  - common_errors.md: Yaygın hatalar ve çözümleri
  - methods.md: Metot tanımlama
  - objects.md: Nesne yapıları
- **reference/**: API referansı
  - variables.md: Built-in değişkenler (open, high, low, close, volume)
  - constants.md: Sabit değerler (color.red, shape.triangle)
  - types.md: Veri tipleri (int, float, bool, color, string)
  - keywords.md: Dil yapıları (if, else, switch, for, while)
  - functions/: Fonksiyon referansları
    - ta.md: Teknik analiz (RSI, SMA, EMA, MACD)
    - strategy.md: Strateji ve backtesting
    - request.md: Harici veri istekleri
    - drawing.md: Grafik çizimleri
    - collections.md: Diziler, matrisler, haritalar
    - general.md: Genel fonksiyonlar (math, string, input)

## Kullanım

### Soru Sorarken
- "RSI nasıl hesaplanır?" → reference/functions/ta.md
- "Strateji nasıl yazılır?" → reference/functions/strategy.md
- "Neden hata alıyorum?" → concepts/common_errors.md

### Kod Üretirken
1. LLM_MANIFEST.md kontrol et
2. İlgili referans dosyasını bul
3. //@version=6 kullan
4. Ta.* fonksiyonlarını tercih et

## Örnek Kod

```pinescript
//@version=6
indicator("RSI Örneği", overlay=false)
rsi = ta.rsi(close, 14)
plot(rsi, color=color.blue)
hline(70, color=color.red, linestyle=hline.style_dashed)
hline(30, color=color.green, linestyle=hline.style_dashed)
```

## Kaynak

- TradingView Pine Script Reference: https://www.tradingview.com/pine-script-reference/v6/
- Pine Script Docs: https://www.tradingview.com/pine-script-docs/welcome/
