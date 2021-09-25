---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 670c5000d3bebc6723b37a5bce9821fdb069f78a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561669"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d’un tableau existant.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lptbl_
  
> [in] Pointeur vers la table MAPI affectée.
    
 _lpproptagColumnsNew_
  
> [in] Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriétés pour les propriétés à ajouter ou déplacer au début du tableau. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la **fonction MAPIAllocateBuffer.** Utilisé pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la **fonction MAPIFreeBuffer.** Utilisé pour libérer de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoyée

 **S_OK**
  
> L’appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.
    
## <a name="remarks"></a>Remarques

La **fonction HrAddColumns équivaut** à utiliser **HrAddColumnsEx** avec  _lpfnFilterColumns_ définie sur NULL. 
  
## <a name="see-also"></a>Voir aussi



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

