---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436110"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Sépare l'identificateur d'entrée composé d'un objet, généralement un message dans une banque de messages, dans l'identificateur d'entrée de cet objet dans le magasin et dans l'identificateur d'entrée de la Banque.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Paramètres

 _pSession_
  
> dans Pointeur vers la session en cours d'utilisation par l'application cliente. 
    
 _cbEID_
  
> dans Taille, en octets, de l'identificateur d'entrée composée à séparer. 
    
 _pEID_
  
> dans Pointeur vers l'identificateur d'entrée composée à séparer. 
    
 _pcbStoreEID_
  
> remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de la Banque de messages qui contient l'objet. Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, le paramètre _pcbStoreEID_ pointe vers la valeur zéro. 
    
 _ppStoreEID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de la Banque de messages qui contient l'objet. Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, la valeur null est renvoyée dans le paramètre _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de l'objet. Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ . 
    
 _ppMsgEID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de l'objet. Si le paramètre _pEID_ pointe vers un identificateur d'entrée qui n'est pas composé, _ppMsgEID_ pointe vers un pointeur vers une copie de l'identificateur d'entrée incomposé. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l'identificateur spécifié par le paramètre _pEID_ est composé, il est scindé en identificateur d'entrée de l'objet au sein de sa banque de messages et de l'identificateur d'entrée de la Banque. Les chaînes d'identificateur d'entrée non composées sont simplement copiées. L'identificateur composé à séparer est généralement un identificateur créé par la fonction [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La mémoire qui contient le paramètre _pEID_ est publiée lors de l'exécution correcte de cette fonction. L'implémentation appelante est chargée de libérer de la mémoire pour les paramètres de sortie. 
  

