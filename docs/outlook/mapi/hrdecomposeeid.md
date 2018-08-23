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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573368"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Sépare l’identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages, dans l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _cbEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée composés d’être séparées. 
    
 _pEID_
  
> [in] Pointeur vers l’identificateur d’entrée composés d’être séparées. 
    
 _pcbStoreEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de la banque de messages qui contient l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, le paramètre _pcbStoreEID_ pointe sur une valeur égale à zéro. 
    
 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de la banque de messages qui contient l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, NULL est renvoyée dans le paramètre _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, _ppMsgEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée non composés. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre _pEID_ est composée, elle est divisée en l’identificateur d’entrée de l’objet dans sa banque de messages et l’identificateur d’entrée du magasin. Chaînes identificateur d’entrée non composés sont simplement copiés. L’identificateur composé à être séparée est généralement créée par la fonction [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La mémoire qui contient le paramètre _pEID_ est publiée en cas de réussite de cette fonction. Implémentation de l’appelante est chargée de libérer de la mémoire pour les paramètres de sortie. 
  

