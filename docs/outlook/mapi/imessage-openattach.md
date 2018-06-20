---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784138"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Numéro d’index de la pièce jointe à ouvrir, tel que stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe. Ce numéro d’index identifie la pièce jointe dans le message unique et est valide uniquement dans le contexte du message.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la pièce jointe. Transmission NULL génère interface standard de la pièce jointe, ou **IAttach**, renvoyée. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est ouverte. Les indicateurs suivants peuvent être définis : 
    
MAPI_BEST_ACCESS 
  
> Demande que la pièce jointe s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, la pièce jointe doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose d’un accès en lecture seule, la pièce jointe doit être ouvert avec accès en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenAttach** renvoyer avec succès, éventuellement avant la pièce jointe est totalement disponible au client appelant. Si la pièce jointe n’est pas disponible, vous appelez suivante lui peut provoquer une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les pièces jointes sont ouverts avec accès en lecture seule, et les clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture. 
    
 _lppAttach_
  
> [out] Pointeur vers un pointeur vers la pièce jointe ouverte.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La pièce jointe a été ouvert avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::OpenAttach** ouvre la pièce jointe d’un message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour ouvrir une pièce jointe, vous devez avoir accès à son nombre de pièces jointes ou d’une propriété **PR_ATTACH_NUM** . Appelez [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table des pièces jointes du message et la ligne qui représente la pièce jointe à ouvrir. Pour plus d’informations, consultez [ouverture d’une pièce jointe](opening-an-attachment.md) . 
  
N’essayez pas d’ouvrir une pièce jointe à plusieurs reprises ; les résultats sont undefined et varie selon le fournisseur de banque de messages.
  
Vous pouvez demander que la pièce jointe s’ouvre en mode lecture/écriture, au lieu du mode par défaut en lecture seule. Toutefois, si la pièce jointe sera réellement ouvert en mode lecture/écriture est le fournisseur de magasin de message. Vous pouvez modifier la pièce jointe, essayez préparation gérer la défaillance ou vérifier le niveau d’accès qui a été accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp utilisé pour  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI utilise la méthode **IMessage::OpenAttach** pour ouvrir les objets attachment,  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

