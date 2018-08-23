---
title: Messages de rapport MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a56223e909edf89d0f7fe2ba7f6d281509002429
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563680"
---
# <a name="mapi-report-messages"></a>Messages de rapport MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Signaler des messages présenter l’état des informations sur un message à l’expéditeur.
  
Il existe deux types généraux de messages de rapport :
  
- Lisez les rapports d’état.
    
- Rapports d’état de remise.
    
## <a name="read-status-reports"></a>Rapports d’état en lecture

Rapports d’état en lecture sont initiées par les fournisseurs de banque de messages via un appel à la méthode [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) et sont envoyées au destinataire représenté par l’identificateur d’entrée dans le **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) propriété. Rapports d’état en lecture ne sont pas générés automatiquement ; les applications clientes qui doivent recevoir les doivent demander explicitement les.
  
Un rapport de lecture indique que l’indicateur de lecture d’un message a été définie, qui peut se produire lorsque le message est ouvert, imprimer, déplacé ou copié. Si un fournisseur de magasins message génère un rapport de lecture en réponse à un déplacement ou opération de copie dépend où le message est sur le point. S’il est en cours déplacé ou copié dans une autre banque de messages, un sera rapport lecture certainement toujours envoyés. S’il est déplacé ou copié dans le magasin de message en cours, un rapport de lecture peut-être ou la ne peut pas être envoyé. 
  
Un rapport nonread indique que l’indicateur de lecture d’un message n’est pas défini et que le message a été ouvert pas avant d’être placé dans le dossier éléments supprimés ou avant l’expiration d’un délai. Les clients peuvent appeler la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) pour définir ou effacer l’indicateur de lecture d’un message. 
  
## <a name="delivery-status-reports"></a>Rapports d’état de remise

État de remise est reflétée dans un rapport de remise, qui est envoyé lorsqu’un message atteint son destinataire, et dans un rapport de non-remise, qui est envoyé lorsqu’un message n’a pas pu atteindre un destinataire. Rapports d’état de remise sont envoyés au destinataire représentée par l’identificateur d’entrée dans la propriété **PR_REPORT_ENTRYID** ou à l’expéditeur si cette propriété n’est pas présente. 
  
Rapports de remise sont envoyés par demande uniquement et ne pas incluent le message d’origine. Rapports de non-remise sont envoyées automatiquement, sauf si une demande est effectuée pour les supprimer. Rapports de non-remise incluent le message d’origine en tant que pièce jointe à activer le destinataire de l’état de renvoyer le message en cas de quelle que soit bloqué la remise n’est plus un problème. Le message joint ressemble à l’original tel qu’il existait lorsque la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) a été appelée pour l’envoyer à l’origine. 
  
Un ou plusieurs rapports d’état de remise sont générées par des fournisseurs de transport quand ils appellent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . Fournisseurs de transport de composer une liste de destinataires pour un message. Si un destinataire reçoit un rapport et le type de rapport est généré dépend des éléments suivants : 
  
- Rapports de remise accédez aux destinataires que vous définissez la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) sur TRUE avant que le message a été placé dans la banque de messages.
    
- Rapports de non-remise accédez aux destinataires qui n’a pas défini la propriété **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) à FALSE. 
    
Presque toutes les informations nécessaires pour afficher un rapport de non-remise est contenue dans la table de destinataires du message attaché. Certaines propriétés sont à partir de l’état. Pour les rapports de remise, les informations nécessaires sont contenues dans la table de destinataires de l’état et dans certaines propriétés du rapport. 
  
Les rapports sont des messages avec les classes de message distincts, en fonction de la classe du message envoyé. La plupart des fournisseurs de services utilisent une convention d’affectation de noms grâce à laquelle la classe de message est composée de plusieurs composants séparés par des virgules. La première partie est « Report » et la dernière partie est une constante représentant le type de rapport. La partie centrale est réservée pour la classe du message envoyé. Par exemple, comme un rapport de remise utilise la constante reprise après sinistre, la classe de message pour une remise de rapports sur un IPM. Message de Remarque serait **Report.IPM.Note.DR**.
  
Le tableau suivant présente l’une des constantes qui représentent les types de rapports.
  
|**Type de rapport**|**Constante utilisée dans la classe de message**|
|:-----|:-----|
|Read  <br/> |IPNRN  <br/> |
|Suppression du mode lecture  <br/> |IPNNRN  <br/> |
|Remise  <br/> |REPRISE APRÈS SINISTRE  <br/> |
|Non-remise  <br/> |Notification d’échec de remise  <br/> |
   
Clients interactives peuvent afficher des messages d’état à l’aide de formulaires standards fournis par MAPI, ou des formulaires personnalisés qui ont été enregistrés avec le Gestionnaire de formulaire pour la classe de message de l’état. Clients qui reçoivent un rapport de non-remise pour un IPM. Message de Remarque, peut, par exemple, afficher le formulaire MAPI standard qui affiche une liste de destinataires ayant échoués et un motif suggéré pour l’échec. Le formulaire permet également aux utilisateurs de renvoyer le message, si vous le souhaitez. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

