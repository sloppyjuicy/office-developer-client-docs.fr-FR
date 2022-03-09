---
title: Rôle du fournisseur de transport dans le sous-système MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
ms.openlocfilehash: 21134012fd09b7f9205e4ee0813df83045c369e1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379009"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Rôle du fournisseur de transport dans le sous-système MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les bibliothèques de liens dynamiques (DLL) du fournisseur de transport fournissent l’interface entre lepooler MAPI et la partie d’un système de messagerie responsable de l’envoi et de la réception des messages. Lepooler MAPI et le fournisseur de transport fonctionnent ensemble pour gérer les responsabilités d’envoi ou de réception d’un message. Lepooler MAPI charge la DLL du fournisseur de transport lorsqu’elle est utilisée pour la première fois et la libère lorsqu’elle n’est plus nécessaire. Plusieurs fournisseurs de transport peuvent être installés sur le même système, mais MAPI fournit le seul spooler requis.
  
En règle générale, les applications clientes ne communiquent pas directement avec le fournisseur de transport. Au lieu de cela, les clients envoient des messages par le biais d’un fournisseur de magasins et lepooler MAPI envoie les messages sortants au fournisseur de transport approprié et envoie les messages entrants à la magasin de messages appropriée. Lepooler MAPI effectue son travail et effectue ses appels aux fournisseurs de transport lorsque les applications au premier plan sont inactives. Après avoir éventuellement affiché des boîtes de dialogue lorsque le fournisseur de transport est connecté pour la première fois, les fournisseurs de transport fonctionnent en arrière-plan, sauf si le client les appelle pour vider les files d’attente d’envoi et de réception. 
  
Les fournisseurs de transport ont les responsabilités suivantes dans un système de messagerie MAPI :
  
- Inscrivez les types d’adresses qu’ils peuvent accepter avec lepooler MAPI afin que lepooler MAPI puisse envoyer des messages au fournisseur de transport approprié en fonction de l’adresse de destination des messages. Un fournisseur de transport peut inscrire plusieurs types d’adresses. Les fournisseurs de transport peuvent également inscrire des adresses de destinataires spécifiques auprès dupooler MAPI. Les messages adressés à l’une de ces adresses sont envoyés au fournisseur de transport qui a enregistré l’adresse auprès dupooler MAPI. Pour plus d’informations, [voir Fournisseur de transport et Modèle opérationnel dupooler MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Remettre les messages entrants aupooler MAPI. Selon la nature du système de messagerie, un fournisseur de transport peut soit avertir directement lepooler MAPI lorsqu’un nouveau message arrive, soit demander aupooler MAPI d’avertir régulièrement le fournisseur de transport pour vérifier la recherche de nouveaux messages.
    
- Convertissez les propriétés de message MAPI en propriétés de message natives dans le système de messagerie. Par exemple, le fournisseur de transport peut avoir à convertir les adresses de l’expéditeur et du destinataire dans un message sortant en un formulaire acceptable pour le système de messagerie. Certains systèmes de messagerie ne supportent pas toutes les propriétés de message MAPI. Pour plus d’informations sur la conservation des propriétés de message MAPI lors de la livraison de messages à un système de messagerie, voir [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
    
- Inscrire les options de message et de destinataire spécifiques au fournisseur de transport.
    
- Effectuer toute vérification des informations d’identification requises par le système de messagerie.
    
- Accéder aux messages sortants à l’aide de l’objet message qui lui a été transmis par lepooler MAPI.
    
- Traduire le format des messages selon les besoins du système de messagerie sous-jacent.
    
- Indiquez **aupooler** MAPI quels destinataires d’un message sortant le fournisseur de transport a accepté la responsabilité de la gestion en fixant la propriété PR_RESPONSIBILITY ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour ces destinataires.
    
- Informez lepooler MAPI lorsqu’un message entrant doit être géré.
    
- Transmettre les données de message entrant aupooler MAPI à l’aide d’objets de message.
    
- Affectez des valeurs à toutes les propriétés de message MAPI requises sur les messages entrants.
    
- Supprimez le message du système de messagerie sous-jacent après la remise, si nécessaire.
    
- Fournir des informations d’état pour lepooler MAPI et les applications clientes.
    
L’illustration suivante illustre le rôle d’un fournisseur de transport par rapport aux autres composants de l’architecture MAPI.
  
**Rôle du fournisseur de transport dans un système de messagerie**
  
![Rôle du fournisseur de transport dans un système de messagerie](media/xp01.gif "Rôle du fournisseur de transport dans un système de messagerie")
  

