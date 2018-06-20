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
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783280"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**S’applique à**: Outlook 
  
Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur affectation. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Paramètres

 _lppNameId_
  
> [in] Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées. 
    
 _enregistrements CNAME_
  
> [in] Nombre de structures de propriété nommée dans le tableau indiqué par le paramètre _lppNameId_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Un ou plusieurs des structures de nom de propriété spécifié ne sont pas valide. 
    
FALSE 
  
> Les structures de nom de propriété spécifié sont valides.
    
## <a name="remarks"></a>Remarques

La fonction **FBadRglpNameID** peut être utilisée lorsque vous configurez pour un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

