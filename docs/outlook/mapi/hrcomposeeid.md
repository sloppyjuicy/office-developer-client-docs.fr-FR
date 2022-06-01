---
title: HrComposeEID
description: La fonction HrComposeEID crée un identificateur d’entrée composé pour un objet, généralement un message dans un magasin de messages.
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
ms.openlocfilehash: 3b57c44f7f9c7619719e9a7af528b6a08237ab53
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816415"
---
# <a name="hrcomposeeid"></a>HrComposeEID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée un identificateur d’entrée composé pour un objet, généralement un message dans un magasin de messages.
  
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
  
> [in] Pointeur vers la session utilisée par l’application cliente.

 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement du magasin de messages contenant le message ou un autre objet. Si zéro est passé dans le paramètre _cbStoreRecordKey_ , le paramètre  _ppEID_ pointe vers une copie de l’identificateur d’entrée de l’objet.

 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement du magasin de messages qui contient le message ou un autre objet.

 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou d’un autre objet.

 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet.

 _pcbEID_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur retourné.

 _ppEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée retourné. Si la valeur du paramètre  _cbStoreRecordKey_ est supérieure à zéro, le paramètre  _ppEID_ pointe vers un pointeur vers l’identificateur d’entrée composé qui est créé. Si _cbStoreRecordKey_ a la valeur zéro, _ppEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée de l’objet.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composé est créé réside dans un magasin de messages, l’identificateur est créé à partir de l’identificateur d’entrée de l’objet et de la clé d’enregistrement du magasin. Si l’objet n’est pas dans un magasin, autrement dit, si le nombre d’octets de la clé d’enregistrement de magasin passée dans  _cbStoreRecordKey_ est égal à zéro, l’identificateur d’entrée de l’objet est simplement copié.
  
La fonction **HrComposeEID** permet aux applications d’utiliser des objets dans plusieurs magasins à l’aide d’identificateurs d’entrée composés. Une application peut appeler la fonction [HrDecomposeEID](hrdecomposeeid.md) pour fractionner l’identificateur d’entrée composé en ses constituants d’origine.
  
## <a name="see-also"></a>Voir aussi

[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)
