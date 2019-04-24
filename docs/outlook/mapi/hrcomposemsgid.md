---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348047"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une chaîne ASCII représentant un identificateur d'entrée composée pour un objet, généralement un message dans une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

 _pSession_
  
> dans Pointeur vers la session en cours d'utilisation par l'application cliente. 
    
 _cbStoreRecordKey_
  
> dans Taille, en octets, de la clé d'enregistrement de la Banque de messages qui contient le message ou un autre objet. Si la valeur zéro est transmise au paramètre _cbStoreRecordKey_ , le paramètre _pszMsgID_ pointe vers une copie de l'identificateur d'entrée converti en texte. 
    
 _pStoreRecordKey_
  
> dans Pointeur vers la clé d'enregistrement de la Banque de messages qui contient le message ou un autre objet. 
    
 _cbMsgEID_
  
> dans Taille, en octets, de l'identificateur d'entrée du message ou d'un autre objet. 
    
 _pMsgEID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet. 
    
 _pszMsgID_
  
> remarquer Pointeur vers la chaîne ASCII renvoyée. Si le paramètre _cbStoreRecordKey_ est supérieur à zéro, le paramètre _pszMsgID_ pointe vers un identificateur d'entrée composé converti en texte. Si _cbStoreRecordKey_ est égal à zéro, _pszMsgID_ pointe vers un identificateur d'entrée non composé converti en texte. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l'identificateur d'entrée composé est créé réside dans une banque de messages, la chaîne de l'identificateur est créée à partir de l'identificateur d'entrée de l'objet et de la clé d'enregistrement de la Banque. Si l'objet n'est pas dans un magasin, autrement dit, si le nombre d'octets pour la clé d'enregistrement passée dans le paramètre _cbStoreRecordKey_ est égal à zéro, l'identificateur d'entrée de l'objet est simplement copié et converti en chaîne. 
  
L'appel de la fonction **HrComposeMsgID** équivaut à l'appel de la fonction [HrComposeEID](hrcomposeeid.md) , puis à la fonction [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** permet aux applications clientes de fonctionner avec des objets dans plusieurs magasins par le biais de l'utilisation d'identificateurs d'entrée composés. Une application peut appeler la fonction [HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l'identificateur d'entrée composée en ses composants d'origine. 
  

