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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582041"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une chaîne ASCII qui représente un identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente. 
    
 _cbStoreRecordKey_
  
> [in] Taille, en octets, de la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet. Si la valeur zéro est transmise dans le paramètre _cbStoreRecordKey_ , le paramètre _pszMsgID_ pointe vers une copie de l’identificateur d’entrée est converti en texte. 
    
 _pStoreRecordKey_
  
> [in] Pointeur vers la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet. 
    
 _cbMsgEID_
  
> [in] Taille, en octets, de l’identificateur d’entrée du message ou un autre objet. 
    
 _pMsgEID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet. 
    
 _pszMsgID_
  
> [out] Pointeur vers la chaîne retournée ASCII. Si le paramètre _cbStoreRecordKey_ est supérieur à zéro, le paramètre _pszMsgID_ pointe vers un identificateur d’entrée composés convertis en texte. Si _cbStoreRecordKey_ est égale à zéro, points _pszMsgID_ à un identificateur d’entrée non composés convertis en texte. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si le message ou un autre objet pour lequel l’identificateur d’entrée composés est en cours de création se trouve dans une banque de messages, la chaîne d’identificateur est créée à partir d’identificateur d’entrée de l’objet et la clé d’enregistrement du magasin. Si l’objet n’est pas dans une banque, autrement dit, si le nombre d’octets pour la clé d’enregistrement magasin passé dans le paramètre _cbStoreRecordKey_ est égale à zéro, identificateur d’entrée de l’objet est simplement copié et converti en une chaîne. 
  
La fonction **HrComposeMsgID** équivaut à appeler la fonction [HrComposeEID](hrcomposeeid.md) , puis la fonction [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** permet aux applications de client travailler avec des objets dans plusieurs magasins à l’aide d’identificateurs d’entrée composés. Une application peut appeler la fonction [HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l’identificateur d’entrée composés en ses composants d’origine. 
  

