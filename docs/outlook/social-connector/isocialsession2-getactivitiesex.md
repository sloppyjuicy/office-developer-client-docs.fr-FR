---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtient une valeur de type String qui représente une collection d'activités de chacun des utilisateurs spécifiés par le paramètre hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336448"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtient une valeur de type String qui représente une collection d'activités de chacun des utilisateurs spécifiés par le paramètre _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Paramètres

_hashedAddresses_
  
> dans Structure qui spécifie un tableau d'adresses SMTP hachées pour un ensemble d'utilisateurs.
    
_startTime_
  
> dans Heure après laquelle les activités créées sont renvoyées.
    
_activités_
  
> remarquer Chaîne XML qui représente l'ensemble des activités des utilisateurs spécifiés par _hashedAddresses_ sur le réseau social depuis _StartTime_.
    
## <a name="remarks"></a>Remarques

L'OSC appelle **GetActivitiesEx** si le fournisseur OSC prend en charge la synchronisation à la demande des activités. L'OSC stocke les informations renvoyées dans les _activités_ en mémoire. Pour plus d'informations sur l'utilisation et la mise à jour de ces informations en mémoire par le OSC, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
À partir d'Outlook Social Connector 2013, le OSC prend uniquement en charge la synchronisation à la demande des activités et appelle uniquement **GetActivitiesEx** pour obtenir des activités. Pour prendre en charge la recherche des activités à la demande, définissez **cacheActivities** sur **false**et **GetActivities** et **dynamicActivitiesLookupEx** sur **true**, et l'OSC appellera **GetActivitiesEx**.
  
La chaîne XML renvoyée doit être conforme à la définition de schéma pour **activityFeed**, comme défini dans le schéma pour l'extensibilité du fournisseur OSC.
  
Le _hashedAddresses_ sring représente un ensemble d'adresses hachées pour chaque utilisateur affiché dans le volet de personnes. Les adresses SMTP hachées sont chiffrées à l'aide de la fonction de hachage spécifiée par l'élément **hashFunction** dans le code XML des **fonctionnalités** du fournisseur. L'utilisateur ne doit pas nécessairement être un ami de l'utilisateur connecté représenté par la propriété [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
Le paramètre _StartTime_ est une valeur de **Date** au format UTC (temps universel coordonné). Les valeurs d'heure locales doivent être converties en valeurs de **Date** UTC. 
  
Les activités renvoyées par la méthode **GetActivitiesEx** doivent avoir une valeur d'heure de création qui est supérieure à _StartTime_ et inférieure ou égale à **Now**. Si aucune modification n'a été apportée entre **StartTime** et **Now**, le fournisseur doit renvoyer une erreur OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)

