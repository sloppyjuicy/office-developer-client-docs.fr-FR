---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416831"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Layer une interface **IStorage** sur un objet **IStream** . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Pointeur vers l'objet **IUnknown** implémentant **IStream**. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'objet Stream. Les valeurs suivantes peuvent être transmises dans le paramètre _lpInterface_ : null, IID_IStream ou IID_ILockBytes. Le passage de la valeur NULL dans _lpInterface_ revient à passer IID_IStream. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont l'objet de stockage doit être créé par rapport au flux. Le paramètre par défaut est STGSTRM_RESET, qui donne à l'objet de stockage un accès en lecture seule et le démarre à la position zéro du flux. Les indicateurs suivants peuvent être définis dans n'importe quelle combinaison, sauf dans les cas indiqués:
    
STGSTRM_CREATE 
  
> Crée un nouvel objet de stockage pour l'objet Stream. Cet indicateur ne peut pas être défini si l'indicateur STGSTRM_RESET est défini. 
    
STGSTRM_CURRENT 
  
> Démarre le stockage à la position actuelle du flux. Cet indicateur ne peut pas être défini si l'indicateur STGSTRM_RESET est défini. 
    
STGSTRM_MODIFY 
  
> Permet au fournisseur de services appelant d'écrire dans le stockage renvoyé. Cet indicateur ne peut pas être défini si l'indicateur STGSTRM_RESET est défini. 
    
STGSTRM_RESET 
  
> Commence le stockage à la position zéro. Cet indicateur ne peut pas être défini si aucun autre indicateur n'est défini. 
    
 _lppStorageOut_
  
> remarquer Pointeur vers un pointeur vers l'objet **IStorage** renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de banques de messages prennent en charge la fonction **HrIStorageFromStream** à l'aide de l'interface **IStorage** pour les pièces jointes. Les fournisseurs de magasins doivent implémenter l'interface **IStream** . **HrIStorageFromStream** fournit l'interface **IStorage** pour l'objet **IStream** . Il est possible de transmettre une interface **ILockBytes** ou **IStream** dans _lpUnkIn_. 
  

