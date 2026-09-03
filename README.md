# .github

`autodesignlab` Organization 的**公開** Profile Repository。

GitHub 規定：Organization 的公開首頁內容必須放在名為 `.github` 的 **public** repository 的 `profile/README.md`。因此本 repo 必須維持 public，但**不放任何產品程式碼**。

## 目錄結構

```
.github/
├─ profile/
│  └─ README.md   ← GitHub 顯示在 Organization 首頁的 Public View
├─ catalog-info.yaml
├─ .governance/
│  └─ governance.yaml
└─ .github/
   └─ CODEOWNERS
```

## 與 `.github-private` 的分工

| Repository | 可見性 | 顯示對象 | 定位 |
| --- | --- | --- | --- |
| `.github`（本 repo） | **public** | 外部訪客（Public View） | **Website Directory** — 介紹官方站與各知識型站點 |
| [`.github-private`](https://github.com/autodesignlab/.github-private) | private | 組織成員（Member View） | **Engineering Portal** — 治理、平台、開發流程導覽 |

兩者內容刻意不同：對外呈現產品與研究，對內呈現工程入口。

## 內容規則

本 repo 是 public，寫入前務必確認：

- ❌ 不放 Tailscale hostname 或任何 Tailnet 內部網域
- ❌ 不放內部 IP、叢集資訊、Infisical 路徑
- ❌ 不放內部工具與管理後台連結（Developer Portal、CD、叢集管理、監控、遠端開發環境等）
- ❌ 不放治理規範細節（那些屬於 `org-governance`，且為 private）
- ✅ 只放 `*.autodesignlab.org` 的公開站點與公開社群連結

## Pinned Repository

組織內所有產品 Repository 目前皆為 private。GitHub 不會對外部訪客顯示釘選的 private repository，因此公開首頁**不依賴 Pinned Repository**，導覽完全由 `profile/README.md` 的網站連結承擔。

## 治理

| 項目 | 值 |
| --- | --- |
| Type | `docs` |
| Domain | `governance` |
| Governance Level | G2 → 目標 G3 |
| Risk Tier | T2 |
| Branch Profile | `standard`（`main` 走 PR） |

正式規範以 [`org-governance`](https://github.com/autodesignlab/org-governance) 為 Single Source of Truth。
