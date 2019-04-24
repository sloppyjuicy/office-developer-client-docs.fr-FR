---
title: Messages de rapport MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329742"
---
# <a name="mapi-report-messages"></a>Messages de rapport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages de rapport présentent les informations d'État relatives à un message envoyé à son expéditeur.
  
Il existe deux types généraux de messages de rapport:
  
- Lire les rapports d'État.
    
- Rapports d'état de remise.
    
## <a name="read-status-reports"></a>Lire les rapports d'État

Les rapports d'état de lecture sont initiés par les fournisseurs de banques de messages via un appel à la méthode [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) et sont envoyés au destinataire représenté par l'identificateur d'entrée dans le **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) inspecteur. Les rapports d'état de lecture ne sont pas générés automatiquement; les applications clientes qui souhaitent les recevoir doivent explicitement les demander.
  
Un rapport de lecture indique que l'indicateur de lecture d'un message a été défini, ce qui peut se produire lors de l'ouverture, l'impression, le déplacement ou la copie du message. Si un fournisseur de banque de messages génère ou non un rapport de lecture en réponse à une opération de déplacement ou de copie dépend de la destination du message. Si elle est déplacée ou copiée dans une autre banque de messages, un rapport de lecture sera vraisemblablement toujours envoyé. Si elle est déplacée ou copiée dans la Banque de messages actuelle, un rapport de lecture peut être envoyé ou non. 
  
Un rapport non lu indique que l'indicateur de lecture d'un message n'est pas défini et que le message n'a pas été ouvert avant d'être placé dans le dossier éléments supprimés ou avant l'expiration d'une limite de temps. Les clients peuvent appeler la méthode [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) pour définir ou effacer l'indicateur de lecture d'un message. 
  
## <a name="delivery-status-reports"></a>Rapports d'état de remise

L'état de remise est reflété dans un rapport de remise, qui est envoyé lorsqu'un message a atteint le destinataire prévu, et dans un rapport de non-remise, qui est envoyé lorsqu'un message n'a pas pu atteindre un destinataire. Les rapports d'état de remise sont envoyés au destinataire représenté par l'identificateur d'entrée dans la propriété **PR_REPORT_ENTRYID** ou à l'expéditeur si cette propriété n'est pas présente. 
  
Les rapports de remise sont envoyés par demande uniquement et n'incluent pas le message d'origine. Les notifications de non-remise sont envoyées automatiquement sauf si une demande est effectuée pour les supprimer. Les rapports de non-remise incluent le message d'origine en tant que pièce jointe pour permettre au destinataire de l'état de renvoyer le message en cas de blocage de la remise. Le message joint ressemble à l'original tel qu'il existait lors de l'appel de la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour l'envoyer initialement. 
  
Un ou plusieurs rapports d'état de remise sont générés par les fournisseurs de transport lorsqu'ils appellent la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . Les fournisseurs de transport composent une liste de destinataires pour un message. Si un destinataire reçoit ou non un rapport et si le type de rapport qui est généré dépend des éléments suivants: 
  
- Les rapports de remise sont rendus aux destinataires qui définissent la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORDELIVERYREPORTREQUESTED](pidtagoriginatordeliveryreportrequested-canonical-property.md)) sur true avant que le message n'ait été placé dans la Banque de messages.
    
- Les rapports de non-remise sont rendus aux destinataires qui n'ont pas défini la propriété **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORNONDELIVERYREPORTREQUESTED](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) sur false. 
    
Presque toutes les informations nécessaires pour afficher un rapport de non-remise sont contenues dans la table des destinataires du message joint. Quelques propriétés proviennent du rapport lui-même. Pour les rapports de remise, les informations nécessaires sont contenues dans la table de destinataires du rapport et dans quelques propriétés de rapport. 
  
Les rapports sont des messages avec des classes de message distinctes, en fonction de la classe du message envoyé. La plupart des fournisseurs de services utilisent une convention d'affectation de noms qui indique que la classe de message est composée de plusieurs parties séparées par des points. La première partie est «Report» et la dernière est une constante qui représente le type de rapport. La partie centrale est réservée pour la classe du message envoyé. Par exemple, étant donné qu'un rapport de remise utilise la constante DR, la classe de message pour un rapport de remise sur un IPM. Remarque le message doit être **Report. IPM. note. Dr**.
  
Le tableau suivant présente les constantes qui représentent les types de rapports.
  
|**Type de rapport**|**Constante utilisée dans la classe de message**|
|:-----|:-----|
|Lecture  <br/> |IPNRN  <br/> |
|Non lu  <br/> |IPNNRN  <br/> |
|Remise  <br/> |REPRISE  <br/> |
|Livraison incomplète  <br/> |-  <br/> |
   
Les clients interActifs peuvent afficher des messages de rapport à l'aide de formulaires standard fournis par MAPI ou des formulaires personnalisés qui ont été enregistrés avec le gestionnaire de formulaires pour la classe de message de l'État. Clients qui reçoivent un rapport de non-remise pour une IPM. Remarque le message peut, par exemple, afficher le formulaire MAPI standard qui présente la liste des destinataires ayant échoué et un motif suggéré pour l'échec. Le formulaire permet également à l'utilisateur de renvoyer le message, le cas échéant. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

