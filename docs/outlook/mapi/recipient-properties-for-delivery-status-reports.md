---
title: Propriétés du destinataire pour les rapports d’état de remise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1063d1a7a062b8b07d9ff66958efc5e65ef8737e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591310"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Propriétés du destinataire pour les rapports d’état de remise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les propriétés suivantes sont présentes pour les rapports d’état de remise des destinataires. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) n’est pas utilisé dans les rapports de non-remise. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) et **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) sont utilisés uniquement sur les rapports d’absence de remise.
  
**Titre du tableau**

|**Propriété**|**Decription**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Contient la date et l’heure de livraison du message d’origine.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Contient le nom complet d’un objet MAPI donné.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Contient un code de diagnostic qui fait partie d’une non-remise.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Contient une chaîne de caractères qui identifie la classe de message définie par l’expéditeur, telle qu’une note IPM.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Contient une raison codée de non-remise qui fait partie d’une non-remise.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Contient le nom complet d’origine d’une entrée copiée à partir d’un carnet d’adresses vers un carnet d’adresses personnel ou un autre carnet d’adresses accessible en entrée.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Contient l’identificateur d’entrée d’origine d’une entrée copiée à partir d’un carnet d’adresses vers un carnet d’adresses personnel ou un autre carnet d’adresses accessible en écriture.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Contient la clé de recherche d’origine d’une entrée copiée à partir d’un carnet d’adresses vers un carnet d’adresses personnel ou un autre carnet d’adresses accessible en écriture.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Contient le type de destinataire d’un destinataire de message.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Contient du texte facultatif pour un rapport généré par le système de messagerie.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Contient la date et l’heure à laquelle le système de messagerie a généré un rapport.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Contient une clé comparable au binaire qui identifie les objets corrélés pour une recherche.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Contient une valeur utilisée pour associer une icône à une ligne particulière d’un tableau.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Contient le type d’un objet.  <br/> |
   

