---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348061"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un identificateur d'entrée composée pour un objet, généralement un message dans une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

 _pSession_
  
> dans Pointeur vers la session en cours d'utilisation par l'application cliente. 
    
 _cbStoreRecordKey_
  
> dans Taille, en octets, de la clé d'enregistrement de la Banque de messages contenant le message ou un autre objet. Si zéro est transmis dans le paramètre _cbStoreRecordKey_ , le paramètre _ppEID_ pointe vers une copie de l'identificateur d'entrée de l'objet. 
    
 _pStoreRecordKey_
  
> dans Pointeur vers la clé d'enregistrement de la Banque de messages qui contient le message ou un autre objet. 
    
 _cbMsgEID_
  
> dans Taille, en octets, de l'identificateur d'entrée du message ou d'un autre objet. 
    
 _pMsgEID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet. 
    
 _pcbEID_
  
> remarquer Pointeur vers la taille, en octets, de l'identificateur retourné. 
    
 _ppEID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné. Si la valeur du paramètre _cbStoreRecordKey_ est supérieure à zéro, le paramètre _ppEID_ pointe vers un pointeur vers l'identificateur d'entrée composé qui est créé. Si _cbStoreRecordKey_ est égal à zéro, _ppEID_ pointe vers un pointeur vers une copie de l'identificateur d'entrée de l'objet. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l'identificateur d'entrée composé est créé réside dans une banque de messages, l'identificateur est créé à partir de l'identificateur d'entrée de l'objet et de la clé d'enregistrement de la Banque. Si l'objet n'est pas dans un magasin, autrement dit, si le nombre d'octets pour la clé d'enregistrement passée dans _cbStoreRecordKey_ est égal à zéro, l'identificateur d'entrée de l'objet est simplement copié. 
  
La fonction **HrComposeEID** permet aux applications de travailler avec des objets dans plusieurs magasins via l'utilisation d'identificateurs d'entrée composés. Une application peut appeler la fonction [HrDecomposeEID](hrdecomposeeid.md) pour fractionner l'identificateur d'entrée composée en ses composants d'origine. 
  
## <a name="see-also"></a>Voir aussi



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

