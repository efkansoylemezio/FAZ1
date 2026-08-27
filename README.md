# secure-starter

Güvenlik sertleştirmesi yapılmış TypeScript proje şablonu.
Her yeni projeye bunu kopyalayarak başla.

## Kurulum

```bash
npm install
npx husky init   # pre-commit hook'u aktifleştirir
```

## Güvenlik katmanları

1. **gitleaks** — her commit'te secret taraması (pre-commit hook)
2. **GitHub Actions CI** — test + `npm audit` + gitleaks
3. **Dependabot** — haftalık bağımlılık güncellemeleri
4. **Secret scanning + push protection** — GitHub repo ayarlarından AÇ
5. **Branch protection** — `main`'e direkt push yasak

## Kurallar

- `.env` asla commit edilmez → `.env.example` kullan
- Sızan key = ölü key → hemen rotate et
- `main` dalına sadece PR ile
