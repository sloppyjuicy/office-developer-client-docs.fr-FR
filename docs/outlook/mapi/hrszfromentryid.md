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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783560"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**S’applique à**: Outlook 
  
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
  

