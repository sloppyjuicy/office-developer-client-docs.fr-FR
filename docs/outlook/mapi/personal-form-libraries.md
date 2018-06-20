---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784966"
---
# <a name="personal-form-libraries"></a>Bibliothèques de formulaires personnels

  
  
**S’applique à**: Outlook 
  
Comme son nom l’indique, les bibliothèques de formulaires personnels contiennent des formulaires d’intérêt pour un utilisateur particulier. Bibliothèque des formulaires personnels d’un utilisateur est la bibliothèque de formulaires associée à la banque de messages par défaut identifiée dans le profil de l’utilisateur ; chaque profil installé sur une station de travail peut utiliser un magasin distinct par défaut et par conséquent, une bibliothèque de formulaires personnels distincts. Une bibliothèque de formulaires personnels peut contenir les copies des formulaires qui figurent également dans les autres bibliothèques de formulaires en plus des autres formes.
  
Une bibliothèque de formulaires personnels est implémentée dans le tableau contenu associé du dossier racine de la banque de messages par défaut d’un utilisateur — si qui réside sur un serveur ou localement sur le poste de travail est non significatifs. Si la banque de messages par défaut de l’utilisateur est stockée sur le poste de travail, bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d’accéder aux formulaires local au lieu de via le réseau. Il est également formulaires disponible pour les utilisateurs qui travaillent en mode hors connexion, qui peuvent se produire lorsque les utilisateurs souhaitent prendre leurs formulaires avec eux sur des ordinateurs portables et sont sans accès à un réseau.
  
Les propriétés et l’implémentation sous-jacente des entrées de la bibliothèque des formulaires personnels incluent une propriété de « ID conteneur » qui identifie le conteneur principal qui l’entrée locale doit être synchronisée avec. Cela peut être l’identificateur d’un dossier arbitraire qui contienne les formulaires. Cette option est utile si vous utilisez un gestionnaire de formulaire personnalisé qui prend en charge un type de bibliothèque de formulaires de l’organisation ; le Gestionnaire de formulaire se chargera de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires de l’organisation. Cela probablement se produit lorsque le Gestionnaire de formulaire a été chargé, mais il peut se produire théoriquement à tout moment.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

