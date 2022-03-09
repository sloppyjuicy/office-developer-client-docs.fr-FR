---
title: Interaction avec le spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
ms.openlocfilehash: a062412ad93d2c44c54fe174a44395a180c68913
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371316"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interaction avec le spooler MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les méthodes de l’interface [IXPLogon : IUnknown](ixplogoniunknown.md) sont utilisées par lepooler MAPI lors de l’appel du fournisseur de transport. Il devrait être possible pour la plupart des types de fournisseurs de transport d’implémenter la plupart de ces méthodes afin qu’elles retournent rapidement. Cela est souhaitable, car si le retour d’une méthode prend beaucoup de temps, elle doit être décomposée avec des appels aupooler MAPI pour libérer l’UC pour d’autres tâches. 
  
Lepooler MAPI effectue son travail et effectue ses appels aux fournisseurs de transport lorsque les applications au premier plan sont inactives. Après avoir éventuellement affiché des boîtes de dialogue lorsque le fournisseur de transport est connecté pour la première fois (régi par des indicateurs transmis de MAPI au fournisseur de transport), les fournisseurs de transport fonctionnent en arrière-plan, sauf si le client l’appelle pour vider les files d’attente d’envoi et de réception. Le  purgement des files d’attente est la seule fois où un fournisseur de transport n’a pas besoin de libérer le processeur, puis uniquement si l’utilisateur est informé qu’une action potentiellement longue est en cours. Lepooler MAPI demande généralement à un fournisseur de transport de vider ses files d’attente en réponse à une action de l’utilisateur, de sorte que le fournisseur de transport n’a généralement rien à faire pour s’assurer que l’utilisateur est informé.
  
Un fournisseur de transport peut décider indépendamment de vider une file d’attente et d’utiliser les bits STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne d’état pour informer lepooler MAPI qu’il souhaite attirer l’attention afin de pouvoir faire le travail. La ligne d’état est mise à jour à l’aide de la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Dans ce cas, le fournisseur de transport doit probablement afficher un indicateur de progression ou une autre interface pour informer l’utilisateur qu’une longue action est en cours. 
  
Étant donné que l’activité réseau prend souvent plus de 0,2 seconde, les fournisseurs de transport doivent, dans la mesure du possible, utiliser des demandes réseau asynchrones. Cela leur permet de lancer une demande, de libérer l’UC en appelant lepooler MAPI, et lorsque lepooler MAPI leur donne à nouveau le contrôle, pour vérifier si leur demande réseau est terminée. Si ce n’est pas encore fait, ils libèrent de nouveau l’UC en appelant lepooler MAPI avec la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) . 
  
Pendant le traitement des messages, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) et [IXPLogon::EndMessage](ixplogon-endmessage.md) [et pendant IXPLogon::StartMessage](ixplogon-startmessage.md), le fournisseur de transport effectue généralement de nombreux appels sur les objets qui lui sont exposés par lepooler MAPI. Dans le cadre de sa gestion de ces objets, lepooler MAPI aide le fournisseur de transport à se comporter de manière appropriée en tant que processus en arrière-plan en se donnent le cas échéant. Un fournisseur de transport nécessitant un traitement time-critical peut déclarer une section critique aupooler MAPI à l’aide de la méthode objet de prise en charge [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . Dans ce cas, l’UC est libérée uniquement sur les appels **SpoolerYield** explicites du fournisseur de transport jusqu’à ce que le fournisseur de transport termine le traitement de section critique par un autre appel à **SpoolerNotify**.
  
> [!NOTE]
> Ce n’est pas la même chose qu’une section Win32 critique. Cette opération ne doit être effectuée que lorsque le fournisseur de transport a besoin d’un contrôle en temps réel des ressources externes telles que la lecture de données entrantes à partir d’une ligne de télécopie. Étant donné que cela augmente la priorité du processus depooler MAPI et peut entraîner le non-réponse de la station de travail pendant toute la durée de l’opération, il est bon d’informer l’utilisateur qu’une action potentiellement longue est en cours et de fournir un indicateur de progression si possible. 
  

