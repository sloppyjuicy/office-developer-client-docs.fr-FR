---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aeeaf871750a6175b7f0746c4c92801dd058bdaa
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634547"
---
# <a name="hrcomposeeid"></a>HrComposeEID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée un identificateur d’entrée composé pour un objet, généralement un message dans une magasin de messages.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |

```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Paramètres

 _psession_
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente.

 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement de la boutique de messages qui détient le message ou un autre objet. Si zéro est transmis dans le paramètre _cbStoreRecordKey_ , le paramètre  _ppEID_ pointe vers une copie de l’identificateur d’entrée de l’objet.

 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement de la magasin de messages qui contient le message ou un autre objet.

 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou d’un autre objet.

 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet.

 _pcbEID_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur renvoyé.

 _ppEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé. Si la valeur du paramètre  _cbStoreRecordKey_ est supérieure à zéro, le paramètre  _ppEID_ pointe vers un pointeur vers l’identificateur d’entrée composé créé. Si _cbStoreRecordKey_ est zéro, _ppEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée de l’objet.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composée est créé réside dans une magasin de messages, l’identificateur est créé à partir de l’identificateur d’entrée de l’objet et de la clé d’enregistrement de la boutique. Si l’objet ne se trouve pas dans une banque, c’est-à-dire, si le nombre d’bytes pour la clé d’enregistrement de la banque transmise dans  _cbStoreRecordKey_ est zéro, l’identificateur d’entrée de l’objet est simplement copié.
  
La **fonction HrComposeEID** permet aux applications de travailler avec des objets dans plusieurs magasins via l’utilisation d’identificateurs d’entrée composés. Une application peut appeler la [fonction HrDecomposeEID](hrdecomposeeid.md) pour fractionner l’identificateur d’entrée composé en ses constituants d’origine.
  
## <a name="see-also"></a>Consultez aussi

[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)
