---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422473"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d'une table existante.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil. h  <br/> |
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
  
> dans Pointeur vers le tableau MAPI affecté.
    
 _lpproptagColumnsNew_
  
> dans Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacer au début du tableau. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction **MAPIAllocateBuffer** . Permet d'allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction **MAPIFreeBuffer** . Permet de libérer de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoyée

 **S_OK**
  
> L'appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.
    
## <a name="remarks"></a>Remarques

La fonction **HrAddColumns** est équivalente à l'utilisation de **HrAddColumnsEx** avec _lpfnFilterColumns_ définie sur null. 
  
## <a name="see-also"></a>Voir aussi



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

