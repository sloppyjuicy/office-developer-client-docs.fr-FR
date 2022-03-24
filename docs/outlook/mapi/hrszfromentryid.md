---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d2fe1047f56a46c9aba2e778bf4343f27cfcd997
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725855"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Encode un identificateur d’entrée dans une chaîne ASCII. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Paramètres

 _cb_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par le paramètre  _pentry_ . 
    
 _pentry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée à coder. 
    
 _psz_
  
> [out] Pointeur vers la chaîne ASCII renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les [fonctions HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** permettent de convertir les formats de chaîne et binaires des identificateurs d’entrée. Avec MAPI, vous devez utiliser des structures avec des données binaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La **fonction HrSzFromEntryID** alloue de la mémoire pour la chaîne ASCII à l’aide de la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

