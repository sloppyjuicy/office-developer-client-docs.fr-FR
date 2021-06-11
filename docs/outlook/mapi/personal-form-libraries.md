---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420408"
---
# <a name="personal-form-libraries"></a>Bibliothèques de formulaires personnels

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Comme son nom l’indique, les bibliothèques de formulaires personnels contiennent des formulaires d’intérêt pour un utilisateur particulier. La bibliothèque de formulaires personnels d’un utilisateur est la bibliothèque de formulaires associée à la magasin de messages par défaut identifiée dans le profil de l’utilisateur . chaque profil installé sur une station de travail peut utiliser un magasin par défaut distinct, et par conséquent, une bibliothèque de formulaires personnelle distincte. Une bibliothèque de formulaires personnels peut contenir des copies de formulaires qui sont également contenues dans d’autres bibliothèques de formulaires en plus d’autres formulaires.
  
Une bibliothèque de formulaires personnels est implémentée dans la table des contenus associés du dossier racine dans la magasin de messages par défaut d’un utilisateur , que celle-ci réside sur un serveur ou localement sur la station de travail de l’utilisateur soit sans importance. Si la boutique de messages par défaut de l’utilisateur est stockée sur la station de travail de l’utilisateur, les bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d’accéder aux formulaires localement et non sur le réseau. Il met également les formulaires à la disposition des utilisateurs qui travaillent hors connexion, ce qui peut se produire lorsque les utilisateurs souhaitent prendre leurs formulaires avec eux sur des ordinateurs portables et qu’ils n’ont pas accès à un réseau.
  
Les propriétés et l’implémentation sous-jacente des entrées de bibliothèque de formulaires personnels incluent une propriété « Container ID » qui identifie un conteneur maître avec qui l’entrée locale doit être synchronisée. Il peut s’agit de l’identificateur d’un dossier arbitraire qui contient des formulaires. Cela est utile si vous utilisez un gestionnaire de formulaires personnalisé qui prend en charge une sorte de bibliothèque de formulaires à l’échelle de l’organisation ; Le gestionnaire de formulaires se charge de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires à l’échelle de l’organisation. Cela se produira probablement lors du chargement du gestionnaire de formulaires, mais peut théoriquement se produire à tout moment.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

