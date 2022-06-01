---
title: HrComposeMsgID
description: La fonction HrComposeMsgID crée une chaîne ASCII représentant un identificateur d’entrée composé pour un objet, généralement un message dans un magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
ms.openlocfilehash: da01bd69a81a4544a9e9acd1d1e95f072fbf5915
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816905"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée une chaîne ASCII représentant un identificateur d’entrée composé pour un objet, généralement un message dans un magasin de messages.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |

```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Paramètres

 _psession_
  
> [in] Pointeur vers la session utilisée par l’application cliente.

 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement du magasin de messages qui contient le message ou un autre objet. Si zéro est passé dans le paramètre _cbStoreRecordKey_ , le paramètre  _pszMsgID_ pointe vers une copie de l’identificateur d’entrée converti en texte.

 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement du magasin de messages qui contient le message ou un autre objet.

 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou d’un autre objet.

 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet.

 _pszMsgID_
  
> [out] Pointeur vers la chaîne ASCII retournée. Si le paramètre  _cbStoreRecordKey_ est supérieur à zéro, le paramètre  _pszMsgID_ pointe vers un identificateur d’entrée composé converti en texte. Si  _cbStoreRecordKey_ a la valeur zéro, _pszMsgID_ pointe vers un identificateur d’entrée non managé converti en texte.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composé est créé réside dans un magasin de messages, la chaîne d’identificateur est créée à partir de l’identificateur d’entrée de l’objet et de la clé d’enregistrement du magasin. Si l’objet n’est pas dans un magasin, autrement dit, si le nombre d’octets de la clé d’enregistrement de magasin passée dans le paramètre _cbStoreRecordKey_ est égal à zéro, l’identificateur d’entrée de l’objet est simplement copié et converti en chaîne.
  
L’appel de la fonction **HrComposeMsgID** équivaut à appeler la fonction [HrComposeEID](hrcomposeeid.md) , puis la fonction [HrSzFromEntryID](hrszfromentryid.md) .
  
 **HrComposeMsgID** permet aux applications clientes d’utiliser des objets dans plusieurs magasins à l’aide d’identificateurs d’entrée composés. Une application peut appeler la fonction [HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l’identificateur d’entrée composé en ses composants d’origine.
  