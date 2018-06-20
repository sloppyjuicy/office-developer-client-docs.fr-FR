---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783513"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**S’applique à**: Outlook 
  
Ajoute ou déplacer des colonnes au début d’une table existante.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes et des fournisseurs de services.  <br/> |
   
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
  
> [in] Pointeur vers le tableau MAPI affecté.
    
 _lpproptagColumnsNew_
  
> [in] Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacées vers le début de la table. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction **MAPIAllocateBuffer** . Utilisé pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction **MAPIFreeBuffer** . Utilisé pour libérer de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoy�e

 **S_OK**
  
> L’appel a réussi et les colonnes spécifiées ont été déplacés ou ajoutés.
    
## <a name="remarks"></a>Remarques

La fonction **HrAddColumns** est équivalente à l’utilisation de **HrAddColumnsEx** avec _lpfnFilterColumns_ la valeur NULL. 
  
## <a name="see-also"></a>Voir aussi



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

