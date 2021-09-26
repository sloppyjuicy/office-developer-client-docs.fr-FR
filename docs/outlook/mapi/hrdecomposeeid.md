---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b8b1f2d590616a30464181bde9bb0d0ad989bb5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610817"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Sépare l’identificateur d’entrée composé d’un objet, généralement un message dans une magasin de messages, dans l’identificateur d’entrée de cet objet dans la boutique et dans l’identificateur d’entrée de la boutique.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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

 _psession_
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _cbEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée composée à séparer. 
    
 _pEID_
  
> [in] Pointeur vers l’identificateur d’entrée composé à séparer. 
    
 _pcbStoreEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de la boutique de messages qui contient l’objet. Si le  _paramètre pEID_ pointe vers un identificateur d’entrée non fourni, le paramètre  _pcbStoreEID_ pointe sur une valeur de zéro. 
    
 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé de la boutique de messages qui contient l’objet. Si le _paramètre pEID_ pointe vers un identificateur d’entrée non saisie, NULL est renvoyé dans le _paramètre ppStoreEID._ 
    
 _pcbMsgEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de l’objet. Si le _paramètre pEID_ pointe vers un identificateur d’entrée non fourni, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID._ 
    
 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé de l’objet. Si le paramètre  _pEID_ pointe vers un identificateur d’entrée noncompound,  _ppMsgEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée non saisie. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre  _pEID_ est composé, il est divisé en identificateur d’entrée de l’objet dans sa magasin de messages et l’identificateur d’entrée de la boutique. Les chaînes d’identificateur d’entrée non saisie sont simplement copiées. L’identificateur composé à séparer est généralement un identificateur créé par [la fonction HrComposeEID.](hrcomposeeid.md) 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La mémoire qui contient le  _paramètre pEID_ est libérée à la fin de cette fonction. L’implémentation d’appel est chargée de libérer de la mémoire pour les paramètres de sortie. 
  

