---
title: Rôle du fournisseur de transport dans le sous-système MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356618"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Rôle du fournisseur de transport dans le sous-système MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les bibliothèques de liens dynamiques (dll) du fournisseur de transport fournissent l'interface entre le spouleur MAPI et la partie d'un système de messagerie responsable de l'envoi et de la réception des messages. Le spouleur MAPI et le fournisseur de transport collaborent pour gérer les responsabilités liées à l'envoi ou à la réception d'un message. Le spouleur MAPI charge la DLL du fournisseur de transport lorsqu'il est utilisé pour la première fois et le libère lorsqu'il n'est plus nécessaire. Plusieurs fournisseurs de transport peuvent être installés sur le même système, mais MAPI fournit le spouleur requis.
  
Les applications clientes ne communiquent généralement pas directement avec le fournisseur de transport. Au lieu de cela, les clients envoient des messages via un fournisseur de banque et le spouleur MAPI envoie des messages sortants au fournisseur de transport approprié et remet les messages entrants à la Banque de messages appropriée. Le spouleur MAPI travaille et effectue ses appels aux fournisseurs de transport lorsque les applications de premier plan sont inactives. Après avoir éventuellement affiché des boîtes de dialogue lors de la première connexion du fournisseur de transport, les fournisseurs de transport fonctionnent en arrière-plan, sauf s'ils sont appelés par le client pour vider les files d'attente d'envoi et de réception. 
  
Les fournisseurs de transport ont les responsabilités suivantes dans un système de messagerie MAPI:
  
- Enregistrer les types d'adresses qu'ils peuvent accepter avec le spouleur MAPI afin que le spouleur MAPI puisse envoyer des messages au fournisseur de transport approprié en fonction de l'adresse de destination des messages. Un fournisseur de transport peut inscrire plusieurs types d'adresses. Les fournisseurs de transport peuvent également enregistrer des adresses de destinataire spécifiques dans le spouleur MAPI. Les messages adressés à l'une de ces adresses seront envoyés au fournisseur de transport qui a inscrit l'adresse auprès du spouleur MAPI. Pour plus d'informations, consultez la rubrique [fournisseur de transport et modèle opérationnel du spouleUR MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Remise de messages entrants au spouleur MAPI. En fonction de la nature du système de messagerie, un fournisseur de transport peut avertir directement le spouleur MAPI lorsqu'un nouveau message arrive ou demander que le spouleur MAPI interroge régulièrement le fournisseur de transport pour vérifier l'arrivée de nouveaux messages.
    
- Convertir les propriétés de message MAPI en et à partir des propriétés de message natives dans le système de messagerie. Par exemple, il se peut que le fournisseur de transport convertisse les adresses de l'expéditeur et du destinataire dans un message sortant vers un formulaire acceptable pour le système de messagerie. Certains systèmes de messagerie ne prennent pas en charge toutes les propriétés de message MAPI. Pour plus d'informations sur la préservation des propriétés de message MAPI lors de la remise de messages à un système de messagerie, consultez [la rubrique développement d'un fournisseur de transport avec TNEF](developing-a-tnef-enabled-transport-provider.md).
    
- Enregistrer les options de message et de destinataire spécifiques au fournisseur de transport.
    
- Effectuer la vérification des informations d'identification requises par le système de messagerie.
    
- Accéder aux messages sortants à l'aide de l'objet message qui lui a été transmis par le spouleur MAPI.
    
- Traduire le format de message comme requis par le système de messagerie sous-jacent.
    
- Informer le spouleur MAPI des destinataires d'un message sortant que le fournisseur de transport a accepté de gérer en définissant la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour ces destinataires.
    
- Informer le spouleur MAPI lorsqu'un message entrant doit être géré.
    
- Transmettre les données des messages entrants au spouleur MAPI à l'aide d'objets message.
    
- Affectez des valeurs à toutes les propriétés de message MAPI requises dans les messages entrants.
    
- Supprimez le message du système de messagerie sous-jacent après la remise, si nécessaire.
    
- Fournir des informations d'État pour le spouleur MAPI et les applications clientes.
    
L'illustration suivante montre le rôle d'un fournisseur de transport par rapport aux autres composants de l'architecture MAPI.
  
**Rôle du fournisseur de transport dans un système de messagerie**
  
![Rôle de fournisseur de transport dans un système de messagerie] (media/xp01.gif "Rôle de fournisseur de transport dans un système de messagerie")
  

