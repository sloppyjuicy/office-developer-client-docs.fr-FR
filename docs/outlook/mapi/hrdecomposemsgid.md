---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404434"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Sépare la représentation ASCII de l’identificateur d’entrée composé d’un objet, généralement un message dans une magasin de messages, dans l’identificateur d’entrée de cet objet dans la boutique et dans l’identificateur d’entrée de la boutique. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _szMsgID_
  
> [in] Chaîne représentant l’identificateur d’entrée de l’objet. 
    
 _pcbStoreEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de la boutique de messages qui contient l’objet. Si le  _paramètre szMsgID_ pointe vers une chaîne d’identificateur d’entrée non saisie, le paramètre  _pcbStoreEID_ pointe sur zéro. 
    
 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé de la boutique de messages qui contient l’objet. Si le _paramètre szMsgID_ pointe vers un identificateur d’entrée non fourni, NULL est renvoyé dans le paramètre _ppStoreEID._ 
    
 _pcbMsgEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de l’objet dans son magasin. Si le paramètre _szMsgID_ pointe vers une chaîne d’identificateur d’entrée non saisie, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID._ 
    
 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers la chaîne d’identificateur d’entrée renvoyée de l’objet dans son magasin. Si le paramètre  _szMsgID_ pointe vers un identificateur d’entrée non fourni,  _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l’identificateur d’entrée non saisie. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre  _szMsgID_ est composé, il est converti à partir d’ASCII et divisé en identificateur d’entrée de l’objet au sein de sa boutique de messages et de l’identificateur d’entrée de la boutique. Les chaînes d’identificateur d’entrée non saisies sont simplement converties et copiées. La chaîne d’identificateur composée à séparer est généralement une chaîne créée par la fonction [HrComposeMsgID.](hrcomposemsgid.md) 
  
Appeler la **fonction HrDecomposeMsgID** équivaut à appeler la fonction [HrEntryIDFromSz,](hrentryidfromsz.md) puis la fonction [HrDecomposeEID.](hrdecomposeeid.md) 
  

