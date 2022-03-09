---
title: IMessageOpenAttach
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d3b8ae41e10d6cffddda52f90212904f66cf1f64
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374984"
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
 
> [in] Numéro d’index de la pièce jointe à ouvrir, tel qu’il est stocké dans la propriété **PR_ATTACH_NUM (**[PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Ce numéro d’index identifie de manière unique la pièce jointe dans le message et n’est valide que dans le contexte du message.

 _lpInterface_
 
> [in] Pointeur vers l’identificateur d’interface (IID) représentant l’interface à utiliser pour accéder à la pièce jointe. La transmission DE NULL entraîne le retour de l’interface standard de la pièce jointe, **ou IAttach**.

 _ulFlags_
 
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est ouverte. Les indicateurs suivants peuvent être définies :

MAPI_BEST_ACCESS
 
> Demande l’ouverture de la pièce jointe avec les autorisations réseau maximales autorisées pour l’utilisateur et l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, la pièce jointe doit être ouverte avec une autorisation de lecture/écriture . Si le client dispose d’un accès en lecture seule, la pièce jointe doit être ouverte avec un accès en lecture seule.

MAPI_DEFERRED_ERRORS
 
> Permet à **OpenAttach** de renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement disponible pour le client appelant. Si la pièce jointe n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur.

MAPI_MODIFY
 
> Demande une autorisation de lecture/écriture. Par défaut, les pièces jointes sont ouvertes avec un accès en lecture seule et les clients ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée.

 _lppAttach_
  
> [out] Pointeur vers un pointeur vers la pièce jointe ouverte.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La pièce jointe a été ouverte avec succès.

## <a name="remarks"></a>Remarques

La **méthode IMessage::OpenAttach** ouvre la pièce jointe d’un message.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ouvrir une pièce jointe, vous devez avoir accès à son numéro de pièce jointe ou **à PR_ATTACH_NUM** propriété. [Appelez IMessage::GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table des pièces jointes du message et localiser la ligne qui représente la pièce jointe à ouvrir. Pour plus [d’informations, voir](opening-an-attachment.md) Ouverture d’une pièce jointe.
  
N’essayez pas d’ouvrir une pièce jointe plusieurs fois ; les résultats ne sont pas définies et dépendent du fournisseur de la boutique de messages.
  
Vous pouvez demander que la pièce jointe soit ouverte en mode lecture/écriture, au lieu du mode lecture seule par défaut. Toutefois, le fournisseur de la boutique de messages doit décider si la pièce jointe sera réellement ouverte en mode lecture/écriture. Vous pouvez soit essayer de modifier la pièce jointe, soit préparer la gestion d’un échec éventuel, soit vérifier le niveau d’accès accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Utilisé pour  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI utilise **la méthode IMessage::OpenAttach** pour ouvrir des objets en pièce jointe,  <br/> |

## <a name="see-also"></a>Voir aussi

[IMessage : IMAPIProp](imessageimapiprop.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
