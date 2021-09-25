---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre hashedAddresses.
ms.openlocfilehash: 152c8750bd92dc1f7ee8bd363d4406ffe1017ac1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563167"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre _hashedAddresses._ 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Paramètres

_hashedAddresses_
  
> [in] Structure qui spécifie un tableau d’adresses SMTP hachées pour un ensemble d’utilisateurs.
    
_startTime_
  
> [in] Heure à laquelle les activités créées sont renvoyées.
    
_activities_
  
> [out] Chaîne XML qui représente l’ensemble des activités des utilisateurs spécifiés par _hashedAddresses_ sur le réseau social depuis _l’heure de début._
    
## <a name="remarks"></a>Remarques

L’OSC appelle **GetActivitiesEx** si le fournisseur OSC prend en charge la synchronisation à la demande des activités. L’OSC stocke les informations renvoyées dans  _les activités_ en mémoire. Pour plus d’informations sur la façon dont OSC utilise et met à jour ces informations en mémoire, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
À compter Outlook Social Connector 2013, OSC prend en charge uniquement la synchronisation à la demande des activités et appelle **uniquement GetActivitiesEx** pour obtenir des activités. Pour prendre en charge la recherche d’activités à la demande, définissez **cacheActivities** sur **false** et **getActivities** et **dynamicActivitiesLookupEx** comme **true**, et l’OSC appelle **GetActivitiesEx**.
  
La chaîne XML renvoyée doit être conforme à la définition de schéma pour **activityFeed**, telle que définie dans le schéma pour l’extensibilité du fournisseur OSC.
  
Le  _hachage hashedAddresses_ représente un ensemble d’adresses hachées pour chaque utilisateur affiché dans le volet Personnes. Les adresses SMTP hachées sont chiffrées à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans le code XML des fonctionnalités **du** fournisseur. L’utilisateur n’a pas besoin d’être un ami de l’utilisateur connecté représenté par la propriété [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) 
  
Le  _paramètre startTime_ est une **valeur Date** en temps universel coordonné (UTC). Les valeurs d’heure locale doivent être converties en valeurs UTC **Date.** 
  
Les activités que la **méthode GetActivitiesEx renvoie** doivent avoir une valeur d’heure de création supérieure à  _l’heure_ de début et inférieure ou égale à **Now**. Si aucune modification n’a été apportée entre **startTime** et **Now,** le fournisseur doit renvoyer OSC_E_NO_CHANGES erreur.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)

