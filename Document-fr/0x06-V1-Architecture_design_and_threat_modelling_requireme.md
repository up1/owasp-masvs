# V1: Exigences Concernant l'Architecture, le Design et le Modèle de Menaces

## Objectif de Contrôle

Dans un monde parfait, la sécurité serait prise en compte tout au long du cycle de développement. Cependant, en réalité la sécurité n'est une considération que tardivement dans le SDLC. Au delà des contrôles techniques, le MASVS exige que des processus soient en place pour garantir que la sécurité a bien été explicitement prise en compte lors de la préparation de l'architecture de l'application mobile et que, pour l'ensemble des composants, les roles fonctionnels et liés à la sécurité sont connus. Dans la mesure où la plupart des applications mobiles agissent en tant que clients de services distants, il est nécessaire de s'assurer que des standards de sécurité pertinents sont aussi appliqués à ces services - tester l'application mobile de manière isolée n'est pas suffisant.

La catégorie “V1” liste les exigences relatives à l'architecture et au design de l'application. Par conséquent, c'est la seule catégorie qui n'est pas reliée à des cas de test techniques dans le Mobile Testing Guide de l'OWASP. Afin de traiter des sujets tels que le modèle de menaces, le SDLC de sécurité, la gestion des clés, le lecteur du MASVS est invité à consulter les projets de l'OWASP dédiés à ces sujets et/ou d'autres standards tel que ceux listés ci-dessous.

<div style="page-break-after: always;">
</div>

## Exigences pour la Validation de la Sécurité

Les exigences pour MASVS-L1 et MASVS-L2 sont listées ci-dessous.

| # | MSTG-ID | Description | L1 | L2 |
| --- | --- | --- | --- | --- |
| **1.1** | MSTG‑ARCH‑1 | Tous les composants de l'application sont identifiés et leur besoin est confirmé. | ✓ | ✓ |
| **1.2** | MSTG‑ARCH‑2 | Les contrôles de sécurité ne sont jamais mis en oeuvre seulement côté client, mais aussi sur les points terminaux distants. | ✓ | ✓ |
| **1.3** | MSTG‑ARCH‑3 | Une architecture de haut niveau concernant l'application mobile et tous les services distants utilisés a été définie et la sécurité a été prise en compte dans cette architecture. | ✓ | ✓ |
| **1.4** | MSTG‑ARCH‑4 | Les données considérées comme sensibles dans le contexte de l'application mobile sont clairement identifiées. | ✓ | ✓ |
| **1.5** | MSTG‑ARCH‑5 | Tous les composants de l'application sont définis en termes des fonctions métier et/ou de sécurité qu'ils apportent. |   | ✓ |
| **1.6** | MSTG‑ARCH‑6 | Un modèle de menaces pour l'application mobile et les services distants associés a été livré et définit les menaces potentielles et les contre-mesures associées. |   | ✓ |
| **1.7** | MSTG‑ARCH‑7 | Tous les contrôles de sécurité ont une implémentation centralisée. |   | ✓ |
| **1.8** | MSTG‑ARCH‑8 | Il existe une politique explicite sur la façon de gérer les clés de cryptographie (dès qu'elles existent) tout au long de leur cycle de vie. Idéalement, un standard de gestion des clés est suivi (tel que NIST SP 800-57). |   | ✓ |
| **1.9** | MSTG‑ARCH‑9 | Un mécanisme pour permettre les mises à jour de l'application mobile existe. |   | ✓ |
| **1.10** | MSTG‑ARCH‑10 | La sécurité est prise en compte tout au long du cycle de développement. |   | ✓ |

## Références

Pour de plus amples informations, il est possible de consulter aussi :

- OWASP Mobile Top 10: M10 - Fonctions superflues : <https://www.owasp.org/index.php/Mobile_Top_10_2016-M10-Extraneous_Functionality>
- OWASP Security Architecture cheat sheet: <https://www.owasp.org/index.php/Application_Security_Architecture_Cheat_Sheet>
- OWASP Thread modelling: <https://www.owasp.org/index.php/Application_Threat_Modeling>
- OWASP Secure SDLC Cheat Sheet: <https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet>
- Microsoft SDL: <https://www.microsoft.com/en-us/sdl/>
- NIST SP 800-57: <http://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf>
