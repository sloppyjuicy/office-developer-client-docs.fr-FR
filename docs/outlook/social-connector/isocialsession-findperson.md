---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au paramètre userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787606"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au paramètre _userID_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_userId_
  
> [in] Un ID d’utilisateur de réseau social, adresse SMTP ou nom complet d’une personne.
    
_résultat_
  
> [out] Chaîne XML qui représente une ou plusieurs personnes qui correspondent aux informations d’identification spécifiées par le paramètre _userId_ . 
    
## <a name="remarks"></a>Remarques

Si une ou plusieurs personnes correspondent à la demande **FindPerson** , cette méthode retourne les informations pour les personnes dans le paramètre de _résultat_ . La chaîne XML de _résultat_ doit être conformes à la définition de schéma pour des **amis**, telle que définie dans le schéma pour l’extensibilité de fournisseur Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

