---
title: HrDecomposeEID
description: Cet article décrit la fonction HrDecomposeEID et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: c391bcfead2aa2379ee80ea212f50d8c37ef3db5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817906"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Sépare l’identificateur d’entrée composé d’un objet, généralement un message dans un magasin de messages, en l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin.
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers la session utilisée par l’application cliente.

 _cbEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée composé à séparer.

 _pEID_
  
> [in] Pointeur vers l’identificateur d’entrée composé à séparer.

 _pcbStoreEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée du magasin de messages qui contient l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée noncompound, le paramètre  _pcbStoreEID_ pointe vers une valeur de zéro.

 _ppStoreEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée retourné du magasin de messages qui contient l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée noncompound, NULL est retourné dans le paramètre _ppStoreEID_ .

 _pcbMsgEID_
  
> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée noncompound, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .

 _ppMsgEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée retourné de l’objet. Si le paramètre _pEID_ pointe vers un identificateur d’entrée noncompound, _ppMsgEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée noncompound.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre  _pEID_ est composé, il est divisé en identificateur d’entrée de l’objet dans son magasin de messages et l’identificateur d’entrée du magasin. Les chaînes d’identificateur d’entrée noncompound sont simplement copiées. L’identificateur composé à séparer est généralement créé par la fonction [HrComposeEID](hrcomposeeid.md) .
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La mémoire qui contient le paramètre  _pEID_ est libérée une fois cette fonction terminée. L’implémentation appelante est chargée de libérer de la mémoire pour les paramètres de sortie.
  