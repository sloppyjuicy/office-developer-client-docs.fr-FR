---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 67c86f39898b4bd0c019b9b3095c9449e6e60b1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567320"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre toutes les propriétés du message et marquer le message comme étant prêt à être envoyé.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont un message est envoyé. Vous pouvez définir l’indicateur suivant :
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message immédiatement. Cet indicateur n’est pas en cours d’utilisation.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_RECIPIENTS 
  
> Table des destinataires du message est vide.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::SubmitMessage** marque un message comme prêts à être transmis. MAPI transmet les messages au système de messagerie sous-jacent dans l’ordre dans lequel ils sont marqués pour l’envoi. En raison de cette fonctionnalité, un message peut rester dans une banque de messages pendant un certain temps avant que le système de messagerie sous-jacent peut prendre la responsabilité de celui-ci. L’ordre de réception à la destination est le contrôle de votre système de messagerie sous-jacent et ne correspond pas nécessairement à l’ordre dans lequel les messages ont été envoyés. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Appelez la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour l’enregistrer, puis vérifiez la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message. Si l’indicateur MSGFLAG_RESEND est défini, appelez [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** met à jour le type de destinataire et la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour tous les destinataires du message à renvoyer.
  
## <a name="notes-to-callers"></a>Notes aux appelants

**SubmitMessage** retourne tous les pointeurs vers le message et ses messages associés sous-objets, dossiers, pièces jointes, flux, tableaux et ainsi de suite ne sont plus valides. MAPI ne permet pas d’opérations supplémentaires sur ces pointeurs, à l’exception de l’appel de leurs méthodes **IUnknown::Release** . MAPI est conçue pour qu’après avoir appelé **SubmitMessage** , vous devez libérer le message et tous les sous-objets. Toutefois, si **SubmitMessage** renvoie une valeur d’erreur indiquant les informations manquantes ou incorrectes, le message reste ouvert et les pointeurs restent valides. 
  
Pour annuler une opération d’envoi, obtenir et de stocker un pointeur vers la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message avant l’envoi du message. Identificateur d’entrée d’un message est non valide après que le message a été envoyé, il est nécessaire pour l’enregistrer avant d’appeler **SubmitMessage**. Pour annuler l’envoi, pointez sur le paramètre _lpEntryId_ cet identificateur d’entrée et appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI utilise la méthode **IMessage::SubmitMessage** pour envoyer le message sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

