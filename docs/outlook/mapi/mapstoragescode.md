---
title: MapStorageSCode
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 733d50f324d1d27d7b089bc6dbc43835f7d21f67
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63716353"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cartes valeur de retour SCODE d’un objet de stockage OLE à un type HRESULT. 
  
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
  
> [in] Valeur de retour MAPI SCODE à partir d’un objet de stockage OLE à ma mappé à une valeur HRESULT.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la valeur attendue.
    
MAPI_E_CALL_FAILED 
  
> La fonction ne peut pas trouver de valeur correspondante.
    
## <a name="remarks"></a>Remarques

MAPI fournit la **fonction MapStorageSCode** pour l’utilisation interne des composants MAPI qui basent leurs implémentations de message sur la DLL de message. Étant donné que ces composants ouvrent eux-mêmes le stockage OLE, ils doivent être en mesure de maculer les valeurs d’erreur renvoyées pour les problèmes liés au stockage OLE à une valeur HRESULT. 
  
Pour plus d’informations, voir [Structured Stockage](structured-storage-in-mapi.md). 
  

