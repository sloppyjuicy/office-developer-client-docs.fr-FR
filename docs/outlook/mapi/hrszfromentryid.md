---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567593"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Code un identificateur d’entrée en une chaîne ASCII. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Paramètres

 _cb_
  
> [in] Taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _pentry_ . 
    
 _pentry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée qui doivent être codées. 
    
 _psz_
  
> [out] Pointeur vers la chaîne retournée ASCII.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions [HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** fournissent la conversion entre les formats binaires d’identificateurs d’entrée de chaîne. MAPI, vous devez utiliser les structures des données binaires. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La fonction **HrSzFromEntryID** alloue de la mémoire de la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

