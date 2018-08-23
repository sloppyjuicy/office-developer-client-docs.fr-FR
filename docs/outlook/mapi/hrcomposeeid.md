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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564814"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement de la banque de message contenant le message ou un autre objet. Si la valeur zéro est transmise dans le paramètre _cbStoreRecordKey_ , le paramètre _ppEID_ pointe vers une copie de l’identificateur d’entrée de l’objet. 
    
 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet. 
    
 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou un autre objet. 
    
 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet. 
    
 _pcbEID_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur retourné. 
    
 _ppEID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée. Si la valeur du paramètre _cbStoreRecordKey_ est supérieure à zéro, le paramètre _ppEID_ pointe vers un pointeur vers l’identificateur d’entrée composés qui est créé. Si _cbStoreRecordKey_ est égale à zéro, _ppEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée de l’objet. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composés est en cours de création se trouve dans une banque de messages, l’identificateur est créé à partir d’identificateur d’entrée de l’objet et la clé d’enregistrement du magasin. Si l’objet n’est pas dans une banque, autrement dit, si le nombre d’octets pour la clé d’enregistrement magasin passé _cbStoreRecordKey_ est égale à zéro, identificateur d’entrée de l’objet est simplement copié. 
  
La fonction **HrComposeEID** permet aux applications de travailler avec des objets dans des magasins de plusieurs identificateurs d’entrée composés grâce à l’utilisation. Une application peut appeler la fonction [HrDecomposeEID](hrdecomposeeid.md) pour fractionner l’identificateur d’entrée composés en ses composants d’origine. 
  
## <a name="see-also"></a>Voir aussi



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

