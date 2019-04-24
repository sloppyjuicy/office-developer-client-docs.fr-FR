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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349230"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre toutes les propriétés du message et marque le message comme étant prêt à être envoyé.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs utilisés pour contrôler le mode d'envoi d'un message. L'indicateur suivant peut être défini:
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message immédiatement. Cet indicateur n'est pas en cours d'utilisation.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_RECIPIENTS 
  
> La table des destinataires du message est vide.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage:: SubmitMessage** marque un message comme étant prêt à être transmis. MAPI transmet des messages au système de messagerie sous-jacent dans l'ordre dans lequel ils sont marqués pour l'envoi. En raison de cette fonctionnalité, un message peut rester dans une banque de messages pendant un certain temps avant que le système de messagerie sous-jacent puisse le prendre en charge. L'ordre de réception à la destination se trouve dans le contrôle du système de messagerie sous-jacent et ne correspond pas nécessairement à l'ordre dans lequel les messages ont été envoyés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message pour l'enregistrer, puis vérifiez la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message. Si l'indicateur MSGFLAG_RESEND est défini, appelez [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md). **PrepareSubmit** met à jour le type de destinataire et la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour tous les destinataires dans le message de renvoi.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **SubmitMessage** renvoie, tous les pointeurs vers le message et ses sous-objets associés les messages, les dossiers, les pièces jointes, les flux, les tables, etc., ne sont plus valides. MAPI n'autorise pas d'autres opérations sur ces pointeurs, à l'exception de l'appel de leurs méthodes **IUnknown:: Release** . MAPI est conçu de telle sorte qu'après l'appel de **SubmitMessage** , vous devez libérer le message et tous les sous-objets associés. Toutefois, si **SubmitMessage** renvoie une valeur d'erreur indiquant que les informations sont manquantes ou incorrectes, le message reste ouvert et les pointeurs restent valides. 
  
Pour annuler une opération d'envoi, récupérez et stockez un pointeur vers la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message avant l'envoi du message. Étant donné que l'identificateur d'entrée d'un message n'est pas valide une fois que le message a été envoyé, il est nécessaire de l'enregistrer avant d'appeler **SubmitMessage**. Pour annuler l'envoi, pointez le paramètre _lpEntryId_ vers cet identificateur d'entrée et appelez [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |**CFolderDlg:: OnSubmitMessage** <br/> |MFCMAPI utilise la méthode **IMessage:: SubmitMessage** pour envoyer le message sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

