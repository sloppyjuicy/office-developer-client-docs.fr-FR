---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 587b8bbb7ac25a7977d8962535f1909464ffc248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571100"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le message en cours est en attente de remise.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont un message est envoyé. Vous pouvez définir l’indicateur suivant :
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message même si elle ne peut pas être envoyé immédiatement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIMessageSite::SubmitMessage** pour demander qu’un message est en attente de remise. Le site de message doit appeler la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d’envoyer le message. Le message n’a pas besoin avoir été précédemment enregistré, car **SubmitMessage** doit provoquer le message d’être enregistré si le message a été modifié. Après le retour de **SubmitMessage**, le formulaire doit rechercher un message en cours et puis faire disparaître si aucune n’existe. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::SubmitMessage** pour enregistrer le message. Tout d’abord, il appelle la méthode **IPersistMessage::HandsOffMessage** , et il appelle ensuite **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

