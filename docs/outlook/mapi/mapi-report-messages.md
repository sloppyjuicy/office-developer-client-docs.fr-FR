---
title: Messages de rapport MAPI
description: Les messages de rapport MAPI présentent des informations d’état sur un message à son expéditeur. Les deux types sont les rapports d’état de lecture et les rapports d’état de remise.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
ms.openlocfilehash: 448d760665004c62120b9787475cbff6f20b741c
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828002"
---
# <a name="mapi-report-messages"></a>Messages de rapport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages de rapport présentent des informations d’état sur un message à son expéditeur.
  
Il existe deux types généraux de messages de rapport :
  
- Lire les rapports d’état.
    
- Rapports d’état de remise.
    
## <a name="read-status-reports"></a>Lire les rapports d’état

Les rapports d’état de lecture sont lancés par les fournisseurs de magasins de messages via un appel à la méthode [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) et sont envoyés au destinataire représenté par l’identificateur d’entrée dans la propriété **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)). Les rapports d’état de lecture ne sont pas générés automatiquement ; les applications clientes qui souhaitent les recevoir doivent les demander explicitement.
  
Un rapport de lecture indique que l’indicateur de lecture d’un message a été défini, ce qui peut se produire lorsque le message est ouvert, imprimé, déplacé ou copié. Le fait qu’un fournisseur de magasin de messages génère ou non un rapport de lecture en réponse à une opération de déplacement ou de copie dépend de l’endroit où le message va. S’il est déplacé ou copié vers un autre magasin de messages, un rapport en lecture sera probablement toujours envoyé. S’il est déplacé ou copié dans le magasin de messages actuel, un rapport de lecture peut ou non être envoyé. 
  
Un rapport non lu indique que l’indicateur de lecture d’un message n’est pas défini et que le message n’a pas été ouvert avant d’être placé dans le dossier Éléments supprimés ou avant l’expiration d’une limite de temps. Les clients peuvent appeler la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) pour définir ou effacer l’indicateur de lecture d’un message. 
  
## <a name="delivery-status-reports"></a>Rapports d’état de remise

L’état de remise se reflète dans un rapport de remise, qui est envoyé lorsqu’un message a atteint son destinataire prévu, et dans un rapport non remis, qui est envoyé lorsqu’un message n’a pas pu atteindre un destinataire. Les rapports d’état de remise sont envoyés au destinataire représenté par l’identificateur d’entrée dans la propriété **PR_REPORT_ENTRYID** ou à l’expéditeur si cette propriété n’est pas présente. 
  
Les rapports de remise sont envoyés par demande uniquement et n’incluent pas le message d’origine. Les rapports non remis sont envoyés automatiquement, sauf si une demande est faite pour les supprimer. Les rapports non remis incluent le message d’origine en tant que pièce jointe pour permettre au destinataire du rapport de renvoyer le message au cas où ce qui bloquerait la remise ne pose plus de problème. Le message joint ressemble à l’original tel qu’il existait lorsque la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) a été appelée pour l’envoyer initialement. 
  
Un ou plusieurs rapports d’état de remise sont générés par les fournisseurs de transport lorsqu’ils appellent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . Les fournisseurs de transport composent une liste de destinataires pour un message. Le fait qu’un destinataire reçoive ou non un rapport et le type de rapport généré dépend des éléments suivants : 
  
- Les rapports de remise sont envoyés aux destinataires qui définissent la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) sur TRUE avant que le message ne soit placé dans le magasin de messages.
    
- Les rapports non distribués sont attribués aux destinataires qui n’ont pas défini la propriété **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) sur FALSE. 
    
Presque toutes les informations nécessaires à l’affichage d’un rapport non remis sont contenues dans la table des destinataires du message joint. Quelques propriétés proviennent du rapport lui-même. Pour les rapports de remise, les informations nécessaires sont contenues dans la table des destinataires du rapport et dans quelques propriétés de rapport. 
  
Les rapports sont des messages avec des classes de messages distinctes, en fonction de la classe du message envoyé. La plupart des fournisseurs de services utilisent une convention d’affectation de noms selon laquelle la classe de message est composée de plusieurs parties séparées par des périodes. La première partie est « Rapport » et la dernière partie est une constante qui représente le type de rapport. La partie centrale est réservée à la classe du message envoyé. Par exemple, étant donné qu’un rapport de remise utilise la récupération d’urgence constante, la classe de message pour un rapport de remise sur un IPM. Le message de note serait **Report.IPM.Note.DR**.
  
Le tableau suivant montre les constantes qui représentent les types de rapports.
  
|**Type de rapport**|**Constante utilisée dans la classe de message**|
|:-----|:-----|
|Lire  <br/> |IPNRN  <br/> |
|Non lu  <br/> |IPNNRN  <br/> |
|Remise  <br/> |DR  <br/> |
|Non remis  <br/> |NDR  <br/> |
   
Les clients interactifs peuvent afficher des messages de rapport à l’aide de formulaires standard fournis par MAPI, ou de formulaires personnalisés qui ont été inscrits auprès du gestionnaire de formulaires pour la classe de message du rapport. Clients qui reçoivent un rapport non remis pour un IPM. Le message de note, par exemple, peut afficher le formulaire MAPI standard qui présente une liste des destinataires ayant échoué et une raison suggérée pour l’échec. Le formulaire permet également à l’utilisateur de renvoyer le message, si vous le souhaitez. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Messages](mapi-messages.md)

