---
title: HrIStorageFromStream
description: Cet article décrit HrIStorageFromStream, il fournit une syntaxe, des paramètres, une valeur de retour et des remarques supplémentaires.
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
ms.openlocfilehash: a000bd652998ba4c55ccb40abac65dcf4d7240c6
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817276"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Superpose une interface **IStorage** à un objet **IStream** . 
  
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
  
> [in] Pointeur vers l’objet **IUnknown** implémentant **IStream**. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet stream. L’une des valeurs suivantes peut être passée dans le paramètre _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes. Le passage de NULL dans  _lpInterface_ revient à passer IID_IStream. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent la façon dont l’objet de stockage doit être créé par rapport au flux. Le paramètre par défaut est STGSTRM_RESET, ce qui donne à l’objet de stockage un accès en lecture seule et le démarre à la position zéro du flux. Les indicateurs suivants peuvent être définis dans n’importe quelle combinaison, sauf comme indiqué :
    
STGSTRM_CREATE 
  
> Crée un objet de stockage pour l’objet stream. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_CURRENT 
  
> Démarre le stockage à la position actuelle du flux. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_MODIFY 
  
> Permet au fournisseur de services appelant d’écrire dans le stockage retourné. Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini. 
    
STGSTRM_RESET 
  
> Démarre le stockage à la position zéro. Cet indicateur ne peut pas être défini si un autre indicateur est défini. 
    
 _lppStorageOut_
  
> [out] Pointeur vers un pointeur vers l’objet **IStorage** retourné. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages prennent en charge la fonction **HrIStorageFromStream** à l’aide de l’interface **IStorage** pour les pièces jointes. Les fournisseurs de magasin doivent implémenter l’interface **IStream** . **HrIStorageFromStream** fournit l’interface **IStorage** pour l’objet **IStream** . Il est possible de passer une interface **ILockBytes** ou **IStream** dans  _lpUnkIn_. 
  

