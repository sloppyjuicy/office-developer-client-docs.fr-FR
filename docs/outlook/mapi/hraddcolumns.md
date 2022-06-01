---
title: HrAddColumns
description: Cet article décrit la fonction HrAddColumns et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
ms.openlocfilehash: e33fc99f569a5ac0eba72747cbd5fb692308d8b9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816422"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d’une table existante.
  
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
  
> [in] Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriété pour les propriétés à ajouter ou à déplacer au début de la table. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction **MAPIAllocateBuffer** . Utilisé pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction **MAPIFreeBuffer** . Utilisé pour libérer de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoyée

 **S_OK**
  
> L’appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.
    
## <a name="remarks"></a>Remarques

La fonction **HrAddColumns** équivaut à utiliser **HrAddColumnsEx** avec  _lpfnFilterColumns_ défini sur NULL. 
  
## <a name="see-also"></a>Voir aussi



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

