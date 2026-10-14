# Changelog

Simulateur d'économie unitaire Art again. Versions suivant [SemVer](https://semver.org/lang/fr/), une release GitHub par version.

## [2.0.0] — 2026-10-14

Mise à jour sur la base du sheet « Structure de coût PixelFrame » d'Arthur (14/10/2026).

### Modifié
- **Le coût de revient est maintenant « rendu France »** (= « Total BOM complète » du sheet). En v1, la BOM ne couvrait que le produit type tablette. En v2, elle inclut aussi :
  - middle frame + cadre alu et passe-partout : 18,76 €, nouveau poste ;
  - packaging : 8,93 €, prix provisoire. Il remplace le champ packaging de 18 € de la v1 ;
  - transport Chine → France en aérien : 12,37 €, nouveau poste ;
  - douane : 0 %.
- **Le N&B est séparé en deux modèles** : N&B 150 PPI (ED133UT2/3, l'ancien « N&B ») et N&B 300 PPI (ED133KC1 Carta 1300 + Tcon Himax T2000).
- Cours actualisés au 14/10/2026 : USD 0,8732 → 0,8935 (+2,3 %) et CNY 0,1288 → 0,1335 (+3,6 %).
- Le packaging reste un champ modifiable, puisque son prix est provisoire. Il vaut 9 € par défaut (8,93 € dans le sheet) et remplace la ligne packaging du sheet dans le coût de revient.
- Le prix par défaut passe de 449 € à 400 €, le prix actuel.
- Ajout d'un lien vers le sheet source (en tête de page et dans le pied de page).
- Dans la matrice, les cas de perte sont en bordeaux. Le titre passe en « art again », en minuscules et italique.
- Le champ « Port » devient « Port client offert » (entrepôt France → client). Il est distinct du transport Chine → France.
- La matrice passe à 3 modèles. Chaque cellule montre le CAC max, le profit au CAC saisi et le coût de revient.

### Impact à prix constant (site, 449 €, CAC max au palier ≤ 100)
| Modèle | v1 | v2 | Écart |
|---|---|---|---|
| Couleur | 161 € | 131 € | −30 € |
| N&B 150 PPI | 114 € | 83 € | −31 € |
| N&B 300 PPI | — | 128 € | nouveau |

### Points connus
- Électronique + méca sont estimés par « SeekInk complet − dalle Spectra 6 » pour les trois modèles. Effet de bord : le N&B 300 PPI coûte plus cher à 101–1000 qu'à ≤ 100.
- Middle frame, cadre alu et packaging ne sont chiffrés qu'à 500 unités.
- Le coût unique de la certification CE (≈ 1 340–1 790 €) n'est pas inclus.

## [1.0.0] — 2026-07-30

Première version. BOM produit seul (N&B ED133UT2/3, Couleur Spectra 6) sur 4 paliers. Packaging 18 € et port 12 € en hypothèses.
