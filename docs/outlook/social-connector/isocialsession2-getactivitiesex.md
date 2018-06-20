---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787621"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Paramètres

_hashedAddresses_
  
> [in] Une structure qui spécifie un tableau de hachage SMTP adresses pour un ensemble d’utilisateurs.
    
_heure de début_
  
> [in] Heure après laquelle les activités créées seront retournées.
    
_activités_
  
> [out] Chaîne XML qui représente l’ensemble des activités des utilisateurs spécifiés par _hashedAddresses_ sur le réseau social depuis _l’heure de début_.
    
## <a name="remarks"></a>Remarques

L’OSC appelle **GetActivitiesEx** si le fournisseur OSC prend en charge la synchronisation de la demande d’activités. L’OSC stocke les informations retournées dans les _activités_ en mémoire. Pour plus d’informations sur la façon dont l’OSC utilise et met à jour ces informations en mémoire, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et appelle uniquement pour obtenir des activités **GetActivitiesEx** . Pour prendre en charge de la recherche des activités à la demande, définissez **cacheActivities** comme **false**et **getActivities** et **dynamicActivitiesLookupEx** **a la valeur True**et la OSC appellera **GetActivitiesEx**.
  
La chaîne XML renvoyée doit être conformes à la définition de schéma pour **activityFeed**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC.
  
Le String _hashedAddresses_ représente un ensemble d’adresses de hachage pour chaque utilisateur affiché dans le volet personnes. Les adresses SMTP hachage sont chiffrés à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans du fournisseur **fonctionnalités** XML. L’utilisateur ne dispose pas à un ami de l’utilisateur connecté, représenté par la propriété [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
Le paramètre _startTime_ est une valeur de **Date** en temps universel coordonné (UTC). Valeurs d’heure locale doivent être convertis en valeurs de **Date** UTC. 
  
Activités retournée par la méthode **GetActivitiesEx** doivent avoir une valeur d’heure de création qui est supérieure à _l’heure de début_ et inférieure ou égale à **maintenant**. Si aucune modification n’ont eu lieu entre les **heures de début** et **maintenant**, le fournisseur doit renvoyer une erreur OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)

