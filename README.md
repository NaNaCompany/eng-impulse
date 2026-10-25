# 평균힘 충격량 계산기

같은 축의 평균힘과 작용 시간으로 충격량 계산

- Plan ID: E063
- App: https://nanalab.kr/eng-impulse/
- Repository: https://github.com/NaNaCompany/eng-impulse
- Formula: `J = F_avg Δt`
- Output: 1차원 충격량 J

## Model

Δt>0. F_avg는 같은 축의 시간평균힘이다. 힘의 부호를 유지하며 힘 최대값을 평균값으로 대신하지 않는다. 충돌 피크·힘-시간 곡선은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `5`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
