---
title: IMessageOpenAttach
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMessage OpenAttach, qui ouvre une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
ms.openlocfilehash: a56ee68d7f791336cea7964e1637af435d87ec89
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828459"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

**S’applique à** : Outlook 2013 | Outlook 2016
 
Ouvre une pièce jointe.
 
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Paramètres

 _ulAttachmentNum_
 
> [in] Numéro d’index de la pièce jointe à ouvrir, tel qu’il est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber) de](pidtagattachnumber-canonical-property.md) la pièce jointe. Ce numéro d’index identifie de façon unique la pièce jointe dans le message et n’est valide que dans le contexte du message.

 _lpInterface_
 
> [in] Pointeur vers l’identificateur d’interface (IID) représentant l’interface à utiliser pour accéder à la pièce jointe. Le passage de la valeur NULL entraîne le retour de l’interface standard de la pièce jointe, ou **IAttach**.

 _ulFlags_
 
> [in] Masque de bits des indicateurs qui contrôlent la façon dont la pièce jointe est ouverte. Les indicateurs suivants peuvent être définis :

MAPI_BEST_ACCESS
 
> Demande que la pièce jointe soit ouverte avec le nombre maximal d’autorisations réseau autorisées pour l’utilisateur et l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, la pièce jointe doit être ouverte avec l’autorisation de lecture/écriture ; si le client dispose d’un accès en lecture seule, la pièce jointe doit être ouverte avec un accès en lecture seule.

MAPI_DEFERRED_ERRORS
 
> Permet à **OpenAttach** de retourner correctement, éventuellement avant que la pièce jointe soit entièrement disponible pour le client appelant. Si la pièce jointe n’est pas disponible, un appel ultérieur peut provoquer une erreur.

MAPI_MODIFY
 
> Demande l’autorisation de lecture/écriture. Par défaut, les pièces jointes sont ouvertes avec un accès en lecture seule, et les clients ne doivent pas fonctionner en partant du principe que l’autorisation de lecture/écriture a été accordée.

 _lppAttach_
  
> [out] Pointeur vers un pointeur vers la pièce jointe ouverte.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La pièce jointe a été ouverte avec succès.

## <a name="remarks"></a>Remarques

La méthode **IMessage::OpenAttach** ouvre la pièce jointe d’un message.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ouvrir une pièce jointe, vous devez avoir accès à son numéro de pièce jointe ou **à sa propriété PR_ATTACH_NUM** . Appelez [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table de pièces jointes du message et localiser la ligne qui représente la pièce jointe à ouvrir. Pour plus [d’informations, consultez l’ouverture d’une pièce jointe](opening-an-attachment.md) .
  
N’essayez pas d’ouvrir une pièce jointe plusieurs fois ; les résultats ne sont pas définis et dépendent du fournisseur du magasin de messages.
  
Vous pouvez demander que la pièce jointe soit ouverte en mode lecture/écriture, au lieu du mode de lecture seule par défaut. Toutefois, si la pièce jointe sera réellement ouverte en mode lecture/écriture, c’est au fournisseur du magasin de messages de décider. Vous pouvez essayer de modifier la pièce jointe, vous préparer à gérer un échec éventuel ou vérifier le niveau d’accès accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp utilisé pour  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI utilise la méthode **IMessage::OpenAttach** pour ouvrir des objets pièces jointes,  <br/> |

## <a name="see-also"></a>Voir aussi

[IMessage : IMAPIProp](imessageimapiprop.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
