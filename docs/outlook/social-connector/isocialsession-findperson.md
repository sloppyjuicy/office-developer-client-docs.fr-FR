---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtient une valeur de type String qui représente une ou plusieurs personnes qui correspondent au paramètre userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285370"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtient une valeur de type String qui représente une ou plusieurs personnes qui correspondent au paramètre _userid_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_Identifi_
  
> dans Un ID utilisateur de réseau social, une adresse SMTP ou le nom d'affichage d'une personne.
    
_result_
  
> remarquer Chaîne XML qui représente une ou plusieurs personnes qui correspondent aux informations d'identification spécifiées par le paramètre _userid_ . 
    
## <a name="remarks"></a>Remarques

Si une ou plusieurs personnes correspondent à la demande **FindPerson** , cette méthode renvoie les informations pour ces personnes dans le paramètre _result_ . La chaîne XML de _résultats_ doit être conforme à la définition de schéma pour les **amis**, comme défini dans le schéma pour l'extensibilité du fournisseur Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

