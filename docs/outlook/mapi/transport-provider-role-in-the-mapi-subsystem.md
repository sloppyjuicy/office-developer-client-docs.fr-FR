---
title: Rôle de fournisseur de transport dans le sous-système MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 263370590a35f19482cc5ad7e56c65f6df0087fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581299"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Rôle de fournisseur de transport dans le sous-système MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Transport fournisseur bibliothèques de liens dynamiques (DLL) fournissent l’interface entre le spouleur MAPI et la partie d’un système de messagerie responsable de l’envoi et la réception de messages. Le spouleur MAPI et le fournisseur de transport fonctionnent ensemble pour gérer les responsabilités de l’envoi d’un message ou de recevoir un message. Le spouleur MAPI charge la DLL du fournisseur de transport lorsqu’il est utilisé en premier et libère lorsqu’il n’est plus nécessaire. Plusieurs fournisseurs de transport peuvent être installés sur le même système, mais MAPI fournit un spouleur requis.
  
En règle générale, les applications clientes ne communiquent pas directement avec le fournisseur de transport. Au lieu de cela, clients envoyer des messages via un fournisseur de magasin et le spouleur MAPI envoie les messages sortants vers le fournisseur de transport approprié et remet les messages entrants dans le magasin de message approprié. Le spouleur MAPI s’exécute et effectue ses appels aux fournisseurs de transport lorsque les applications de premier plan sont inactifs. Une fois connecté éventuellement afficher les boîtes de dialogue lorsque le fournisseur de transport est en premier, fournisseurs de transport fonctionnent en arrière-plan, sauf si appelée par le client à purger envoyer et recevoir des files d’attente. 
  
Fournisseurs de transport comportent les responsabilités ci-après dans une système de messagerie MAPI de :
  
- Enregistrer les types d’adresses qu’ils peuvent accepter avec le spouleur MAPI afin que le spouleur MAPI peut envoyer des messages au fournisseur de transport approprié en fonction de l’adresse de destination des messages. Un fournisseur de transport permettre enregistrer plusieurs types d’adresse. Fournisseurs de transport peuvent également enregistrer les adresses des destinataires spécifiques avec le spouleur MAPI. Les messages adressés à une de ces adresses seront envoyées au fournisseur de transport qui inscrit l’adresse avec le spouleur MAPI. Pour plus d’informations, voir [fournisseur de Transport et le modèle opérationnel du spouleur MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Remettre les messages entrants pour le spouleur MAPI. En fonction de la nature du système de messagerie, un fournisseur de transport peut soit directement informer le spouleur MAPI lorsqu’un nouveau message arrive, ou il peut demander que le spouleur MAPI interroger le fournisseur de transport régulièrement pour vérifier les nouveaux messages.
    
- Convertir des propriétés de message MAPI vers et à partir des propriétés de message natives au système de messagerie. Par exemple, le fournisseur de transport peut-être convertir les adresses de l’expéditeur et du destinataire dans un message sortant à un formulaire qui est acceptable pour le système de messagerie. Certains systèmes de messagerie ne prennent pas en charge toutes les propriétés de message MAPI. Pour plus d’informations sur la préservation des propriétés de message MAPI lors de la remise des messages à un système de messagerie, voir [développement d’un fournisseur de Transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
    
- Enregistrez le message et le destinataire options spécifiques au fournisseur de transport.
    
- Effectuer la vérification des informations d’identification requises par le système de messagerie.
    
- Accès aux messages sortants à l’aide de l’objet message lui sont transmises par le spouleur MAPI.
    
- Convertir le format de message comme requis par le système de messagerie sous-jacent.
    
- Informer le spouleur MAPI les destinataires d’un message sortant, le fournisseur de transport a accepté la responsabilité de gestion en définissant la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) des destinataires.
    
- Informer le spouleur MAPI lorsqu’un message entrant doit être gérée.
    
- Passer des données de message entrant pour le spouleur MAPI à l’aide des objets de message.
    
- Affecter des valeurs à toutes les propriétés de message MAPI requises sur les messages entrants.
    
- Supprimer le message à partir du système de messagerie sous-jacent après la livraison, si nécessaire.
    
- Fournissent des informations d’état pour les applications de client et spouleur MAPI.
    
L’illustration suivante montre le rôle d’un fournisseur de transport en ce qui concerne les autres composants de l’architecture MAPI.
  
**Rôle du fournisseur de transport dans un système de messagerie**
  
![Rôle de fournisseur de transport dans un système de messagerie] (media/xp01.gif "Rôle de fournisseur de transport dans un système de messagerie")
  

