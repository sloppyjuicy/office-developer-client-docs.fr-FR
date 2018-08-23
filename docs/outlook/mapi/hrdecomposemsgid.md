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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564625"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Sépare la représentation ASCII de l’identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages, l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _szMsgID_
  
> [in] La chaîne représentant l’identificateur d’entrée de l’objet. 
    
 _pcbStoreEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de la banque de messages qui contient l’objet. Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés chaîne, le paramètre _pcbStoreEID_ pointe sur zéro. 
    
 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de la banque de messages qui contient l’objet. Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés, NULL est renvoyée dans le paramètre _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet dans son magasin. Si le paramètre _szMsgID_ pointe vers une chaîne d’identificateur de l’entrée non composés, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers la chaîne d’identificateur de l’objet dans son magasin entrée retournée. Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés, _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l’identificateur d’entrée non composés. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre _szMsgID_ est composée, il est converti à partir d’ASCII et résulter de l’identificateur d’entrée de l’objet dans sa banque de messages et l’identificateur d’entrée du magasin. Chaînes identificateur d’entrée non composés sont simplement convertis et copiés. La chaîne d’identificateur composés à être séparée est généralement créée par la fonction [HrComposeMsgID](hrcomposemsgid.md) . 
  
La fonction **HrDecomposeMsgID** équivaut à appeler la fonction [HrEntryIDFromSz](hrentryidfromsz.md) , puis la fonction [HrDecomposeEID](hrdecomposeeid.md) . 
  

