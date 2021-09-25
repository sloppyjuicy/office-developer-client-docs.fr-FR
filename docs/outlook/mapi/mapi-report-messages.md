---
title: Messages de rapport MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 383c673a7313bb3a91e35f109399be92f98e215f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575679"
---
# <a name="mapi-report-messages"></a>Messages de rapport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages de rapport présentent des informations d’état sur un message à son expéditeur.
  
Il existe deux types généraux de messages de rapport :
  
- Lire les rapports d’état.
    
- Rapports d’état de remise.
    
## <a name="read-status-reports"></a>Lire les rapports d’état

Les rapports d’état de lecture sont initiés par les fournisseurs de magasins de messages via un appel à la méthode [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) et sont envoyés au destinataire représenté par l’identificateur d’entrée dans la propriété **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)). Les rapports d’état de lecture ne sont pas générés automatiquement ; les applications clientes qui souhaitent les recevoir doivent explicitement les demander.
  
Un rapport de lecture indique que l’indicateur de lecture d’un message a été définie, ce qui peut se produire lorsque le message est ouvert, imprimé, déplacé ou copié. Le fait qu’un fournisseur de magasins de messages génère ou non un rapport de lecture en réponse à une opération de déplacement ou de copie dépend de l’endroit où se déplace le message. S’il est déplacé ou copié dans une autre magasin de messages, un rapport de lecture sera probablement toujours envoyé. S’il est déplacé ou copié dans la boutique de messages actuelle, un rapport de lecture peut être envoyé ou non. 
  
Un rapport non lu indique que l’indicateur de lecture d’un message n’est pas définie et que le message n’a pas été ouvert avant d’être placé dans le dossier Éléments supprimés ou avant l’expiration d’une limite de temps. Les clients peuvent appeler la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) pour définir ou effacer l’indicateur de lecture d’un message. 
  
## <a name="delivery-status-reports"></a>Rapports d’état de remise

L’état de remise est reflété dans un rapport de remise, qui est envoyé lorsqu’un message a atteint son destinataire prévu, et dans un rapport de non remise, qui est envoyé lorsqu’un message n’a pas pu atteindre un destinataire. Les rapports d’état de remise sont envoyés au destinataire représenté par l’identificateur d’entrée dans la propriété **PR_REPORT_ENTRYID** ou à l’expéditeur si cette propriété n’est pas présente. 
  
Les rapports de remise sont envoyés uniquement par demande et n’incluent pas le message d’origine. Les rapports non envoyés sont envoyés automatiquement, sauf si une demande de suppression est faite. Les rapports non remise incluent le message d’origine en tant que pièce jointe pour permettre au destinataire du rapport de renvoyer le message au cas où tout blocage de la remise ne serait plus un problème. Le message joint ressemble à l’original tel qu’il existait lorsque la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) a été appelée pour l’envoyer initialement. 
  
Un ou plusieurs rapports d’état de remise sont générés par les fournisseurs de transport lorsqu’ils appellent la méthode [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) Les fournisseurs de transport composent une liste de destinataires pour un message. Le fait qu’un destinataire reçoit ou non un rapport et le type de rapport généré dépend des données suivantes : 
  
- Les rapports de remise sont envoyés aux destinataires qui définissent la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) sur TRUE avant que le message ne soit placé dans la magasin de messages.
    
- Les rapports non remis sont remis aux destinataires qui n’ont pas PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED **(** [PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) sur FALSE. 
    
Presque toutes les informations nécessaires à l’affichage d’un rapport de non-destinataire sont contenues dans la table des destinataires du message joint. Quelques propriétés sont du rapport lui-même. Pour les rapports de remise, les informations nécessaires sont contenues dans la table des destinataires du rapport et dans quelques propriétés de rapport. 
  
Les rapports sont des messages avec des classes de message distinctes, en fonction de la classe du message envoyé. La plupart des fournisseurs de services utilisent une convention d’attribution de noms selon laquelle la classe de message est composée de plusieurs parties séparées par des périodes. La première partie est « Report » et la dernière est une constante qui représente le type de rapport. La partie intermédiaire est réservée à la classe du message envoyé. Par exemple, comme un rapport de remise utilise la constante DR, la classe de message pour un rapport de remise sur un IPM. Le message de note **serait Report.IPM.Note.DR**.
  
Le tableau suivant indique les constantes qui représentent les types de rapports.
  
|**Type de rapport**|**Constante utilisée dans la classe de message**|
|:-----|:-----|
|Lire  <br/> |IPNRN  <br/> |
|Non lu  <br/> |IPNNRN  <br/> |
|Remise  <br/> |DR  <br/> |
|Non-delivery  <br/> |NDR  <br/> |
   
Les clients interactifs peuvent afficher des messages de rapport à l’aide de formulaires standard fournis par MAPI ou de formulaires personnalisés qui ont été enregistrés auprès du gestionnaire de formulaires pour la classe de message de l’état. Clients qui reçoivent un rapport de non-demande pour un IPM. Le message de note, par exemple, peut afficher le formulaire MAPI standard qui présente la liste des destinataires en échec et une suggestion de motif de l’échec. Le formulaire permet également à l’utilisateur de renvoyer le message, si vous le souhaitez. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Messages](mapi-messages.md)

