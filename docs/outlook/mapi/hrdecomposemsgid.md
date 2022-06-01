---
title: HrDecomposeMsgID
description: Cet article décrit la fonction HrDecomposeMsgID et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
ms.openlocfilehash: 41a7d279515ac2be6f97cd40107ebefef7ffd783
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816891"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

**S’applique à** : Outlook 2013 | Outlook 2016

Sépare la représentation ASCII de l’identificateur d’entrée composé d’un objet, généralement un message dans un magasin de messages, dans l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin.

|Propriété |Valeur |
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

## <a name="parameters"></a>Paramètres

 _psession_

> [in] Pointeur vers la session utilisée par l’application cliente.

 _szMsgID_

> [in] Chaîne représentant l’identificateur d’entrée de l’objet.

 _pcbStoreEID_

> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée du magasin de messages qui contient l’objet. Si le paramètre _szMsgID_ pointe vers une chaîne d’identificateur d’entrée noncompound, le paramètre _pcbStoreEID_ pointe vers zéro.

 _ppStoreEID_

> [out] Pointeur vers un pointeur vers l’identificateur d’entrée retourné du magasin de messages qui contient l’objet. Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée noncompound, NULL est retourné dans le paramètre _ppStoreEID_ .

 _pcbMsgEID_

> [out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet dans son magasin. Si le paramètre _szMsgID_ pointe vers une chaîne d’identificateur d’entrée noncompound, le paramètre  _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .

 _ppMsgEID_

> [out] Pointeur vers un pointeur vers la chaîne d’identificateur d’entrée retournée de l’objet dans son magasin. Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée noncompound, _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l’identificateur d’entrée noncompound.

## <a name="return-value"></a>Valeur renvoyée

Aucun.

## <a name="remarks"></a>Remarques

Si l’identificateur spécifié par le paramètre _szMsgID_ est composé, il est converti à partir d’ASCII et divisé en identificateur d’entrée de l’objet dans son magasin de messages et l’identificateur d’entrée du magasin. Les chaînes d’identificateur d’entrée noncompound sont simplement converties et copiées. La chaîne d’identificateur composé à séparer est généralement créée par la fonction [HrComposeMsgID](hrcomposemsgid.md) .

L’appel de la fonction **HrDecomposeMsgID** équivaut à appeler la fonction [HrEntryIDFromSz](hrentryidfromsz.md) , puis la fonction [HrDecomposeEID](hrdecomposeeid.md) .
