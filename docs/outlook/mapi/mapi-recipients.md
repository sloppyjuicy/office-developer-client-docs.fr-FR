---
title: Destinataires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423691"
---
# <a name="mapi-recipients"></a>Destinataires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage : IMAPIProp](imessageimapiprop.md).
  
Clients acc�dent � un destinataire de message par le biais de sa table des destinataires. Chaque message poss�de une table de destinataires qui contient des informations r�capitulatives sur chacun de ses destinataires. Les colonnes incluses dans le tableau d�pendent de l'�tat du message. Lorsqu'un message est en cours de composition, ses destinataires peuvent avoir uniquement trois colonnes dans la table :
  
- Nom d'affichage, ou **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Type de destinataire, ou **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Identificateur de ligne, ou **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Une fois que le message a subi le processus de résolution de noms, chaque destinataire aura également un identificateur d'entrée, ou une colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Et lorsque le message a �t� envoy�, les lignes dans la table de destinataires ajoute deux colonnes :
  
- Type d'adresse ou **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Responsabilité de transport ou **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) est une propriété d'objet table qui représente la table de destinataires d'un message. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
For more information about how to work with a recipient table, see [Tables de destinataires](recipient-tables.md).
  
En plus utilis�e pour acc�der � une table de destinataires, **PR_MESSAGE_RECIPIENTS** peuvent �tre utilis�es : 
  
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include recipients when copying. For more information see, [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Dans une restriction sous-objet pour indiquer que la restriction de l'enfant doit s'appliquer � des destinataires.
    
Les clients peuvent ajouter des destinataires � un message en copiant des entr�es � partir du carnet d'adresses MAPI ou en cr�ant de nouvelles entr�es. Ces nouvelles entr�es, appel�es uniques, pouvant exister temporairement ou d�finitivement enregistr�es dans un conteneur modifiable. Consid�rant que les destinataires qui proviennent du carnet d'adresses ont des identificateurs d'entr�e associ�s � leur fournisseur de carnet d'adresses, destinataires uniques ont des identificateurs d'entr�e qui sont mis en forme � MAPI. Transport fournisseurs et clients associez entr�e unique identifiers avec diff�rents types d'adresses. 
  
Fournisseurs de transport appeler **IMAPISupport::CreateOneOff** pour cr�er un identificateur d'entr�e unique pour une adresse sur une sortie quand des messages : 
  
- L'adresse appartient � une passerelle.
    
- L'adresse ne peut pas �tre g�r� par un fournisseur de carnet d'adresses dans le profil actif.
    
For more information, see [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Les clients appellent **IAddrBook::CreateOneOff** pour cr�er un identificateur d'entr�e unique pour une adresse sur entrante quand des messages : 
  
- L'adresse est mis en forme comme une adresse unique.
    
- L'adresse est mis en forme comme une adresse Internet.
    
For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).
  
For more information about one-off entry identifiers and addresses, see [Identificateurs d'entr�e unique](one-off-entry-identifiers.md) and [Adresses uniques](one-off-addresses.md).
  
Les propri�t�s d'un destinataire sont une combinaison de propri�t�s de carnet d'adresses et des propri�t�s sp�cifiques aux destinataires. Tous les destinataires ont les propri�t�s d'adresse de base, affect�es par les fournisseurs de carnet d'adresses. Lorsqu'une entr�e est utilis�e en tant que destinataire d'un message sortant, les propri�t�s de l'adresse de base sont copi�es � la structure **ADRLIST** qui conserve les propri�t�s de tous les destinataires d'un message. 
  
Deux propri�t�s qui sont d�finies pour les destinataires sont **PR_RECIPIENT_TYPE** et **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** indique si un destinataire est un serveur principal, copie carbone, copie carbone invisible ou un destinataire � renvoyer. Les trois premiers types sont affect�s � des destinataires sur les messages qui sont envoy�s pour la premi�re fois. 
  
Si un destinataire ne re�oit pas le message et une tentative est effectu�e pour renvoyer, le destinataire est copi� et son type est d�fini sur MAPI_P1 pour indiquer qu'il s'agit d'un destinataire � renvoyer. Si seulement certaines des destinataires re�oivent un message, leurs propri�t�s **PR_RECIPIENT_TYPE** sont marqu�es avec l'ajout de l'indicateur MAPI_SUBMITTED lorsque le message est renvoy�. Les clients sont requises pour g�rer les destinataires principaux ou destinataires avec leurs **PR_RECIPIENT_TYPE** d�fini sur MAPI_TO. Tous les autres types sont facultatifs. 
  
 **PR_RESPONSIBILITY** est d�finie pour indiquer au fournisseur de transport, il doit traiter l'envoi au destinataire ou non. Lorsqu'un message sortant est d'abord envoy�, tous les destinataires d�finissez **PR_RESPONSIBILITY** � FALSE. Comme un fournisseur de transport bas�e sur les revendications de la responsabilit� de l'envoi � une ou plusieurs des destinataires, leurs propri�t�s **PR_RESPONSIBILITY** sont d�finies � TRUE. 
  

