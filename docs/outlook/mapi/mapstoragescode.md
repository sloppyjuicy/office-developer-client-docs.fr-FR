---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357630"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Mappe une valeur de retour SCODE à partir d'un objet de stockage OLE vers un type HRESULT. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Paramètres

 _StgSCode_
  
> dans Valeur de retour de la propriété SCODE MAPI d'un objet de stockage OLE à mapper à une valeur HRESULT.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la valeur attendue.
    
MAPI_E_CALL_FAILED 
  
> La fonction ne parvient pas à trouver une valeur correspondante.
    
## <a name="remarks"></a>Remarques

MAPI fournit la fonction **MapStorageSCode** pour l'utilisation interne des composants MAPI qui basent les implémentations de leurs messages sur la dll du message. Étant donné que ces composants ouvrent le stockage OLE eux-mêmes, ils doivent être en mesure de mapper les valeurs d'erreur renvoyées pour les problèmes liés au stockage OLE vers une valeur HRESULT. 
  
Pour plus d'informations, consultez la rubrique [stockage structuré](structured-storage-in-mapi.md). 
  

