---
title: Interaction avec le spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c8032172ef19fbb01af68058b2e0255e269183a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587893"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interaction avec le spouleur MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les méthodes dans le [IXPLogon : IUnknown](ixplogoniunknown.md) interface utilisés par le spouleur MAPI lors de l’appel du fournisseur de transport. Il doit être possible, pour la plupart des types de fournisseurs de transport pour implémenter la plupart de ces méthodes pour qu’elles retournent rapidement. Il est souhaitable, car si une méthode prend beaucoup de temps à retourner puis il doit être divisée avec appelle de nouveau le spouleur MAPI pour libérer de l’UC pour d’autres tâches. 
  
Le spouleur MAPI s’exécute et effectue ses appels aux fournisseurs de transport lorsque les applications de premier plan sont inactifs. Après affichage éventuellement les boîtes de dialogue lorsque le fournisseur de transport est tout d’abord connecté (régi par les indicateurs passés à partir de MAPI pour le fournisseur de transport), les fournisseurs de transport fonctionnent en arrière-plan, sauf si appelée par le client à vider envoyer et recevoir des files d’attente. Files d’attente de vidage est la seule fois qu’un fournisseur de transport libère pas forcément l’UC, puis uniquement si l’utilisateur est informé qu’une action peut être longue est en cours. Le spouleur MAPI demande généralement qu’un fournisseur de transport purger ses files d’attente en réponse à une action de l’utilisateur, afin que le fournisseur de transport ne doit généralement pas rien à faire pour vous assurer que l’utilisateur est informé.
  
Un fournisseur de transport peut décider de manière indépendante vider une file d’attente et les bits STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état pour informer le spouleur MAPI qu’elle a besoin Attention afin qu’elle peut faire le travail. La ligne d’état est mis à jour à l’aide de la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Dans ce cas le fournisseur de transport doit probablement afficher un indicateur de progression ou une autre interface pour informer l’utilisateur qu’une action de type longue qui se produit. 
  
Étant donné que l’activité réseau prend souvent plus de 0,2 secondes, fournisseurs de transport doivent, si possible, utilisez demandes réseau asynchrones. Cela leur permet de lancer une requête, la version de l’UC en effectuant un rappel pour le spouleur MAPI et le spouleur MAPI leur confère à nouveau contrôle, pour vérifier si leur demande réseau a terminé. Si elle n’est pas encore terminée, ils release à nouveau l’UC en effectuant un rappel pour le spouleur MAPI avec la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) . 
  
Au cours de traitement des messages, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) et [IXPLogon::EndMessage](ixplogon-endmessage.md) et pendant [IXPLogon::StartMessage](ixplogon-startmessage.md), le fournisseur de transport effectue généralement de nombreux appels sur les objets exposés à celui-ci par le spouleur MAPI. Dans le cadre de la gestion de ces objets, le spouleur MAPI permet le fournisseur de transport se comportent correctement en arrière-plan grâce à la production sur son propre le cas échéant. Un fournisseur de transport nécessitant un traitement serré peut déclarer une section critique au spouleur MAPI à l’aide de la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) prise en charge de l’objet. Dans ce cas, l’UC est publié uniquement des appels explicites **SpoolerYield** par le fournisseur de transport jusqu'à ce que le fournisseur de transport termine avec un autre appel à **SpoolerNotify**de traitement de section critique.
  
> [!NOTE]
> Il n’est pas identique à une section critique Win32. Il doit être effectuée uniquement lorsque le fournisseur de transport a besoin en temps réel de contrôle des ressources externes, telles que la lecture de données entrantes à partir d’une ligne de télécopie. Étant donné que cela entraîne la priorité du processus de spouleur MAPI et peut entraîner la station de travail à ne répond pas pendant la durée de l’opération, il est judicieux de signaler à l’utilisateur qu’une action peut être longue est en cours d’exécution et fournir un indicateur de progression dans la mesure du possible. 
  

