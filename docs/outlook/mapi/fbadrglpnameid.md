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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434829"
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
  
> [in] Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées. 
    
 _cNames_
  
> [in] Nombre de structures de propriétés nommées dans le tableau pointés par _le paramètre lppNameId._ 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ou plusieurs des structures de noms de propriété spécifiées ne sont pas valides. 
    
FALSE 
  
> Les structures de noms de propriété spécifiées sont toutes valides.
    
## <a name="remarks"></a>Remarques

La **fonction FBadRglpNameID** peut être utilisée lors de la configuration d’un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

