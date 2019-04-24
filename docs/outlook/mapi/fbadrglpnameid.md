---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341033"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur allocation. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Paramètres

 _lppNameId_
  
> dans Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées. 
    
 _Enregistrements CNAME_
  
> dans Nombre de structures de propriété nommées dans le tableau vers lequel pointe le paramètre _lppNameId_ . 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ou plusieurs des structures de nom de propriété spécifiées ne sont pas valides. 
    
FALSE 
  
> Les structures de nom de propriété spécifiées sont toutes valides.
    
## <a name="remarks"></a>Remarques

La fonction **FBadRglpNameID** peut être utilisée lors de la configuration d'un appel à [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

