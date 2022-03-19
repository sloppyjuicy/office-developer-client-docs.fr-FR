---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 899d529db55d72e7d6c8c486a1a7a86b7029ac38
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629502"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Couches **d’une interface IStorage** sur un **objet IStream** . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Paramètres

 _lpUnkIn_
  
> [in] Pointeur vers **l’objet IUnknown** implémentant **IStream**. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet de flux. L’une des valeurs suivantes peut être transmise dans le paramètre _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes. La transmission de la valeur NULL  _dans lpInterface_ est la même que la transmission IID_IStream. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport au flux. Le paramètre par défaut est STGSTRM_RESET, ce qui donne à l’objet de stockage un accès en lecture seule et le démarre à la position zéro du flux. Les indicateurs suivants peuvent être définies dans n’importe quelle combinaison, sauf comme indiqué :
    
STGSTRM_CREATE 
  
> Crée un objet de stockage pour l’objet stream. Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie. 
    
STGSTRM_CURRENT 
  
> Démarre le stockage à la position actuelle du flux. Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie. 
    
STGSTRM_MODIFY 
  
> Permet au fournisseur de services appelants d’écrire dans le stockage renvoyé. Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie. 
    
STGSTRM_RESET 
  
> Démarre le stockage à la position zéro. Cet indicateur ne peut pas être définie si un autre indicateur est définie. 
    
 _lppStorageOut_
  
> [out] Pointeur vers un pointeur vers l’objet **IStorage** renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages supportent **la fonction HrIStorageFromStream** à l’aide de l’interface **IStorage** pour les pièces jointes. Les fournisseurs du Store doivent implémenter **l’interface IStream** . **HrIStorageFromStream fournit** l’interface **IStorage** pour **l’objet IStream** . Il est possible de transmettre une interface **ILockBytes** ou **IStream** dans  _lpUnkIn_. 
  

