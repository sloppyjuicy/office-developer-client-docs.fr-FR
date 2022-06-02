---
title: IMessageSubmitMessage
description: IMessageSubmitMessage enregistre toutes les propriétés du message et marque le message comme prêt à être envoyé.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
ms.openlocfilehash: 2951938ccf870ee126cdc25be28f621842f7d4ac
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828452"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre toutes les propriétés du message et marque le message comme prêt à être envoyé.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs utilisés pour contrôler la façon dont un message est envoyé. L’indicateur suivant peut être défini :
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message immédiatement. Cet indicateur n’est pas utilisé actuellement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_RECIPIENTS 
  
> La table des destinataires du message est vide.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::SubmitMessage** marque un message comme prêt à être transmis. MAPI transmet les messages au système de messagerie sous-jacent dans l’ordre dans lequel ils sont marqués pour l’envoi. En raison de cette fonctionnalité, un message peut rester dans un magasin de messages pendant un certain temps avant que le système de messagerie sous-jacent puisse en assumer la responsabilité. L’ordre de réception à destination est sous le contrôle du système de messagerie sous-jacent et ne correspond pas nécessairement à l’ordre dans lequel les messages ont été envoyés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour l’enregistrer, puis vérifiez la propriété **PR_MESSAGE_FLAGS** du message ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si l’indicateur MSGFLAG_RESEND est défini, appelez [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** met à jour le type de destinataire et **la propriété PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour tous les destinataires du message de renvoi.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **SubmitMessage** est retourné, tous les pointeurs vers le message et ses sous-objets associés messages, dossiers, pièces jointes, flux, tables, et ainsi de suite ne sont plus valides. MAPI n’autorise pas d’autres opérations sur ces pointeurs, à l’exception de l’appel de leurs méthodes **IUnknown::Release** . MAPI est conçu de telle sorte qu’une fois **SubmitMessage** appelé, vous devez libérer le message et tous les sous-objets associés. Toutefois, si **SubmitMessage** retourne une valeur d’erreur indiquant des informations manquantes ou non valides, le message reste ouvert et les pointeurs restent valides. 
  
Pour annuler une opération d’envoi, récupérez et stockez un pointeur vers la propriété **PR_ENTRYID** du message ([PidTagEntryId](pidtagentryid-canonical-property.md)) avant l’envoi du message. Étant donné que l’identificateur d’entrée d’un message est invalidé une fois le message envoyé, il est nécessaire de l’enregistrer avant d’appeler **SubmitMessage**. Pour annuler l’envoi,  _pointez le paramètre lpEntryId_ sur cet identificateur d’entrée et appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI utilise la méthode **IMessage::SubmitMessage** pour envoyer le message sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

