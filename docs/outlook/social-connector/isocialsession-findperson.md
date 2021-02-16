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
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434794"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au _paramètre userID._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Paramètres

_userId_
  
> [in] ID d’utilisateur de réseau social, adresse SMTP ou nom d’affichage d’une personne.
    
_result_
  
> [out] Chaîne XML qui représente une ou plusieurs personnes qui correspondent aux informations d’identification spécifiées par le _paramètre userId._ 
    
## <a name="remarks"></a>Remarques

Si une ou plusieurs personnes correspondent à la **demande FindPerson,** cette méthode renvoie les informations de ces personnes dans le  _paramètre de_ résultat. La  _chaîne_ XML de résultat doit être conforme à la définition de schéma pour les **amis,** telle que définie dans le schéma pour l’extensibilité du fournisseur Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

