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
ms.openlocfilehash: 9a26d55416d7da20b2915acfda644c50e4d86dc2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378253"
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
  
> [in] Taille, en octets, de l’identificateur d’entrée composé à séparer.

 _pEID_
  
> [in] Pointeur vers l’identificateur d’entrée composé à séparer.

 _pcbStoreEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de la boutique de messages qui contient l’objet. Si le _paramètre pEID_ pointe vers un identificateur d’entrée non saisie, le paramètre  _pcbStoreEID_ pointe sur une valeur de zéro.

 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé de la magasin de messages qui contient l’objet. Si le _paramètre pEID_ pointe vers un identificateur d’entrée non fourni, NULL est renvoyé dans le _paramètre ppStoreEID_ .

 _pcbMsgEID_
  
> [out] Pointeur vers la taille renvoyée, en octets, de l’identificateur d’entrée de l’objet. Si le _paramètre pEID_ pointe vers un identificateur d’entrée non fourni, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .

 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé de l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée noncompound, _ppMsgEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée non saisie.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre  _pEID_ est composé, il est divisé en identificateur d’entrée de l’objet au sein de sa magasin de messages et de l’identificateur d’entrée de la boutique. Les chaînes d’identificateur d’entrée non saisies sont simplement copiées. L’identificateur composé à séparer est généralement un identificateur créé par [la fonction HrComposeEID](hrcomposeeid.md) .
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La mémoire qui contient le  _paramètre pEID_ est libérée à la fin de cette fonction. L’implémentation d’appel est chargée de libérer de la mémoire pour les paramètres de sortie.
  