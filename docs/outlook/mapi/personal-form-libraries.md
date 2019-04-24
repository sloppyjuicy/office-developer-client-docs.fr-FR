---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348446"
---
# <a name="personal-form-libraries"></a>Bibliothèques de formulaires personnels

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Comme son nom l'indique, les bibliothèques de formulaires personnels contiennent des formulaires intéressants pour un utilisateur particulier. La bibliothèque de formulaires personnels d'un utilisateur est la bibliothèque de formulaires associée à la Banque de messages par défaut identifiée dans le profil de l'utilisateur; chaque profil installé sur une station de travail peut utiliser une banque par défaut distincte et, par conséquent, une bibliothèque de formulaires personnels distincte. Une bibliothèque de formulaires personnels peut contenir des copies de formulaires qui sont également contenus dans d'autres bibliothèques de formulaires en plus d'autres formulaires.
  
Une bibliothèque de formulaires personnels est implémentée dans la table des contenus associés du dossier racine de la Banque de messages par défaut d'un utilisateur (qu'elle réside sur un serveur ou localement sur la station de travail de l'utilisateur). Si la Banque de messages par défaut de l'utilisateur est stockée sur la station de travail de l'utilisateur, les bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d'accéder aux formulaires localement plutôt qu'au réseau. Il met également les formulaires à la disposition des utilisateurs qui travaillent en mode hors connexion, ce qui peut se produire lorsque les utilisateurs souhaitent prendre leur forme sur des ordinateurs portables et s'ils ne disposent pas d'un accès à un réseau.
  
Les propriétés et l'implémentation sous-jacente d'entrées de bibliothèque de formulaires personnelles incluent une propriété «ID de conteneur» qui identifie un conteneur maître avec lequel l'entrée locale doit être synchronisée. Il peut s'agir de l'identificateur d'un dossier arbitraire qui contient des formulaires. Cette fonctionnalité est utile si vous utilisez un gestionnaire de formulaires personnalisés qui prend en charge un type de bibliothèque de formulaires à l'échelle de l'Organisation; le gestionnaire de formulaires s'occupe de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires à l'échelle de l'organisation. Cela se produit probablement lorsque le gestionnaire de formulaire a été chargé, mais peut théoriquement se produire à tout moment.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

