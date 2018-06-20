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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783556"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**S’applique à**: Outlook 
  
Couches d’une interface **IStorage** sur un objet **IStream** . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers l’objet **IUnknown** implémentation **IStream**. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet stream. Une des valeurs suivantes peuvent être transmise dans le paramètre _lpInterface_ : IID_ILockBytes, IID_IStream ou NULL. En passant NULL _lpInterface_ est identique au transfert IID_IStream. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet stream. Le paramètre par défaut est STGSTRM_RESET, qui fournit l’accès en lecture seule d’objet stockage et démarre à la position zéro de l’objet stream. Les indicateurs suivants peuvent avoir n’importe quelle combinaison, sauf comme indiqué précédemment :
    
STGSTRM_CREATE 
  
> Crée un nouvel objet de stockage pour l’objet stream. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_CURRENT 
  
> Démarre le stockage à la position actuelle du flux. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_MODIFY 
  
> Permet au fournisseur de service appelant écrire dans le stockage renvoyé. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_RESET 
  
> Stockage commence à la position zéro. Impossible de définir cet indicateur si n’importe quel autre indicateur est défini. 
    
 _lppStorageOut_
  
> [out] Pointeur vers un pointeur vers l’objet **IStorage** renvoyé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Banque de messages fournisseurs prennent en charge la fonction **HrIStorageFromStream** à l’aide de l’interface **IStorage** pour les pièces jointes. Fournisseurs de magasins doivent implémenter l’interface **IStream** . **HrIStorageFromStream** fournit l’interface **IStorage** pour l’objet **IStream** . Il est possible de passer une interface **IStream** dans _lpUnkIn_soit un **ILockBytes** . 
  

