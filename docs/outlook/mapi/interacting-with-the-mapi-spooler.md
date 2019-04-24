---
title: Interaction avec le spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317205"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interaction avec le spouleur MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les méthodes de l'interface [IXPLogon: IUnknown](ixplogoniunknown.md) sont utilisées par le spouleur MAPI lors de l'appel du fournisseur de transport. La plupart des types de fournisseurs de transport doivent être en mesure d'implémenter la plupart de ces méthodes pour qu'elles soient renvoyées rapidement. Ceci est souhaitable car, si une méthode prend beaucoup de temps à retourner, elle doit être répartie avec des appels vers le spouleur MAPI pour libérer le processeur pour d'autres tâches. 
  
Le spouleur MAPI travaille et effectue ses appels aux fournisseurs de transport lorsque les applications de premier plan sont inactives. Après avoir affiché éventuellement des boîtes de dialogue lorsque le fournisseur de transport est connecté pour la première fois (régi par des indicateurs transmis par MAPI au fournisseur de transport), les fournisseurs de transport fonctionnent en arrière-plan, sauf s'ils sont appelés par le client pour vider les files d'attente d'envoi et de réception. Le vidage des files d'attente est la seule fois qu'un fournisseur de transport n'a pas besoin de libérer le processeur, et uniquement si l'utilisateur est informé qu'une action potentiellement longue est en cours. Le spouleur MAPI demande généralement à un fournisseur de transport de vider ses files d'attente en réponse à une action de l'utilisateur, de sorte que le fournisseur de transport n'a pas besoin de faire quoi que ce soit pour s'assurer que l'utilisateur est informé.
  
Un fournisseur de transport peut décider indépendamment de vider une file d'attente et d'utiliser les bits STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne d'État pour informer le spouleur MAPI qu'il souhaite attention afin qu'il puisse accomplir le travail. La ligne d'État est mise à jour à l'aide de la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . Dans ce cas, le fournisseur de transport doit probablement afficher un indicateur de progression ou une autre interface pour informer l'utilisateur qu'une longue action a lieu. 
  
Étant donné que l'activité réseau prend souvent plus de 0,2 secondes, les fournisseurs de transport doivent, chaque fois que cela est possible, utiliser des demandes réseau asynchrones. Cela leur permet de lancer une demande, de libérer l'UC en rappelant le spouleur MAPI, et lorsque le spouleur MAPI les communique de nouveau, afin de vérifier si la demande réseau est terminée. Si elle n'a pas encore été exécutée, elle libère le processeur en rappelant le spouleur MAPI à l'aide de la méthode [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) . 
  
Pendant le traitement des messages, entre [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) et [IXPLogon:: EndMessage](ixplogon-endmessage.md) et pendant [IXPLogon:: StartMessage](ixplogon-startmessage.md), le fournisseur de transport effectue généralement de nombreux appels sur les objets exposés par le spouleur MAPI. Dans le cadre de sa gestion de ces objets, le spouleur MAPI aide le fournisseur de transport à se comporter de manière appropriée en tant que processus d'arrière-plan en s'appropriant ses propres cas. Un fournisseur de transport requérant un traitement à temps critique peut déclarer une section critique dans le spouleur MAPI à l'aide de la méthode d'objet de prise en charge [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . Dans ce cas, l'UC est libérée uniquement sur les appels **SpoolerYield** explicites par le fournisseur de transport jusqu'à ce que le fournisseur de transport termine le traitement de la section critique avec un autre appel à **SpoolerNotify**.
  
> [!NOTE]
> Il ne s'agit pas d'une section critique Win32. Cette opération doit être réalisée uniquement lorsque le fournisseur de transport a besoin d'un contrôle en temps réel des ressources externes, telles que la lecture des données entrantes à partir d'une ligne de télécopie. Étant donné que cela augmente la priorité du processus de spouleur MAPI et peut entraîner le blocage de la station de travail pendant la durée de l'opération, il est judicieux d'informer l'utilisateur qu'une action potentiellement longue est en cours et de fournir un indicateur de progression, le cas échéant. 
  

