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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348089"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Sépare la représentation ASCII de l'identificateur d'entrée composé d'un objet, généralement un message dans une banque de messages, dans l'identificateur d'entrée de cet objet dans le magasin et l'identificateur d'entrée du magasin. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

## <a name="parameters"></a>Paramètres

 _pSession_
  
> dans Pointeur vers la session en cours d'utilisation par l'application cliente. 
    
 _szMsgID_
  
> dans La chaîne représentant l'identificateur d'entrée de l'objet. 
    
 _pcbStoreEID_
  
> remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de la Banque de messages qui contient l'objet. Si le paramètre _szMsgID_ pointe vers une chaîne d'identificateur d'entrée non composée, le paramètre _pcbStoreEID_ pointe vers zéro. 
    
 _ppStoreEID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de la Banque de messages qui contient l'objet. Si le paramètre _szMsgID_ pointe vers un identificateur d'entrée non composé, la valeur null est renvoyée dans le paramètre _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de l'objet dans son magasin. Si le paramètre _szMsgID_ pointe vers une chaîne d'identificateur d'entrée non composée, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ . 
    
 _ppMsgEID_
  
> remarquer Pointeur vers un pointeur vers la chaîne d'identificateur d'entrée renvoyée de l'objet dans son magasin. Si le paramètre _szMsgID_ pointe vers un identificateur d'entrée décomposée, _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l'identificateur d'entrée de composition. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l'identificateur spécifié par le paramètre _szMsgID_ est composé, il est converti à partir de ASCII et scindé en l'identificateur d'entrée de l'objet dans sa banque de messages et l'identificateur d'entrée du magasin. Les chaînes d'identificateur d'entrée non composées sont simplement converties et copiées. La chaîne d'identificateur composée à séparer est généralement une chaîne créée par la fonction [HrComposeMsgID](hrcomposemsgid.md) . 
  
L'appel de la fonction **HrDecomposeMsgID** équivaut à l'appel de la fonction [HrEntryIDFromSz](hrentryidfromsz.md) , puis à la fonction [HrDecomposeEID](hrdecomposeeid.md) . 
  

