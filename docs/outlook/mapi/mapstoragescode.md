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
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784793"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**S’applique à**: Outlook 
  
Cartes SCODE renvoie la valeur d’un objet de stockage OLE à un type de valeur HRESULT. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Paramètres

 _StgSCode_
  
> [in] Valeur de retour MAPI SCODE à partir d’un objet de stockage OLE à mapper à une valeur HRESULT.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et a renvoyé la valeur attendue.
    
MAPI_E_CALL_FAILED 
  
> La fonction ne peut pas trouver une valeur correspondante.
    
## <a name="remarks"></a>Remarques

MAPI fournit la fonction **MapStorageSCode** pour l’utilisation interne des composants MAPI que leurs implémentations de message dans la DLL de message de base. Étant donné que ces composants ouvrir le stockage OLE eux-mêmes, ils doivent pouvoir mapper des valeurs d’erreur renvoyés de problèmes avec le stockage OLE à une valeur HRESULT. 
  
Pour plus d’informations, voir [Stockage structuré](structured-storage-in-mapi.md). 
  

