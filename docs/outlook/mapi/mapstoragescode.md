---
title: MapStorageSCode
description: Décrit la syntaxe, les paramètres et la valeur de retour de MapStorageSCode, qui mappe une valeur de retour SCODE d’un objet de stockage OLE à un type HRESULT.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
ms.openlocfilehash: c836b699a0afe63e2beaf8feb962d6e14cceacf4
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828510"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cartes une valeur de retour SCODE d’un objet de stockage OLE vers un type HRESULT. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Paramètres

 _StgSCode_
  
> [in] MapI SCODE renvoie la valeur d’un objet de stockage OLE à mapper à une valeur HRESULT.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et retourné la valeur attendue.
    
MAPI_E_CALL_FAILED 
  
> La fonction ne trouve pas de valeur correspondante.
    
## <a name="remarks"></a>Remarques

MAPI fournit la fonction **MapStorageSCode** pour l’utilisation interne des composants MAPI qui basent leurs implémentations de message sur la DLL de message. Étant donné que ces composants ouvrent eux-mêmes le stockage OLE, ils doivent être en mesure de mapper les valeurs d’erreur retournées pour les problèmes liés au stockage OLE à une valeur HRESULT. 
  
Pour plus d’informations, consultez [Structured Stockage](structured-storage-in-mapi.md). 
  

