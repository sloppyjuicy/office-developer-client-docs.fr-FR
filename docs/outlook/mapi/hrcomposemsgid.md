---
title: HrComposeMsgID
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 178575fb52f9c44038b785cb60805302c8e09d6d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371960"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée une chaîne ASCII représentant un identificateur d’entrée composé pour un objet, généralement un message dans une magasin de messages.
  
|||
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente.

 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement de la boutique de messages qui contient le message ou un autre objet. Si zéro est transmis dans le paramètre _cbStoreRecordKey_ , le paramètre  _pszMsgID_ pointe vers une copie de l’identificateur d’entrée converti en texte.

 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement de la magasin de messages qui contient le message ou un autre objet.

 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou d’un autre objet.

 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet.

 _pszMsgID_
  
> [out] Pointeur vers la chaîne ASCII renvoyée. Si le  _paramètre cbStoreRecordKey_ est supérieur à zéro, le paramètre  _pszMsgID_ pointe vers un identificateur d’entrée composé converti en texte. Si  _cbStoreRecordKey_ a la valeur zéro, _pszMsgID_ pointe vers un identificateur d’entrée non complet converti en texte.

## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composée est créé réside dans une magasin de messages, la chaîne d’identificateur est créée à partir de l’identificateur d’entrée de l’objet et de la clé d’enregistrement de la boutique. Si l’objet ne se trouve pas dans une banque, c’est-à-dire, si le nombre d’caractères de la clé d’enregistrement de la banque transmise dans le paramètre _cbStoreRecordKey_ est zéro, l’identificateur d’entrée de l’objet est simplement copié et converti en chaîne.
  
Appeler la **fonction HrComposeMsgID** équivaut à appeler la fonction [HrComposeEID](hrcomposeeid.md) , puis la [fonction HrSzFromEntryID](hrszfromentryid.md) .
  
 **HrComposeMsgID** permet aux applications clientes de travailler avec des objets dans plusieurs magasins via l’utilisation d’identificateurs d’entrée composés. Une application peut appeler la [fonction HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l’identificateur d’entrée composé en ses constituants d’origine.
  