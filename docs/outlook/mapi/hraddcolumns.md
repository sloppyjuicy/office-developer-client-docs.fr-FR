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
ms.openlocfilehash: e25b313f4bd86ca03b05392a4a5a3118cd891345
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720627"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d’un tableau existant.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services. |
   
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
  
> [in] Pointeur vers la **fonction MAPIAllocateBuffer** . Utilisé pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la **fonction MAPIFreeBuffer** . Utilisé pour libérer de la mémoire. 
    
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

