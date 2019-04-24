---
title: Moteur d'inActivité MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d8d591c02bb621c16a1d1b46272b19573ea79785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346808"
---
# <a name="mapi-idle-engine"></a>Moteur d'inActivité MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI offre plusieurs fonctions, appelées «moteur inactif». Ces fonctions permettent aux clients, aux fournisseurs de carnets d'adresses et aux fournisseurs de banques de messages d'effectuer diverses tâches pendant les temps de ralentissement dans la session ou en réponse à un temps de ralentissement. Par exemple, les clients et les fournisseurs de services peuvent différer les opérations lentes ou fermer des fichiers qui sont restés inutilisés pendant une longue période. En règle générale, les fournisseurs de transport n'utilisent pas le moteur inactif car la méthode **IXPLogon:: Idle** prend sa place. Pour plus d'informations, consultez la rubrique [IXPLogon:: Idle](ixplogon-idle.md).
  
Pour utiliser le moteur inactif, les clients et les fournisseurs de services créent une fonction de rappel qui contient les tâches qui doivent se produire lorsque le sous-système MAPI est inactif. Lorsque MAPI détecte le temps d'inactivité, il appelle cette fonction de rappel. La fonction de rappel suit le prototype **FNIDLE** , défini comme suit: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Pour plus d'informations, consultez la rubrique [FNIDLE](fnidle.md).
  
Les fonctions qui composent le moteur inactif sont les suivantes:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Pour enregistrer une fonction de rappel, les clients et les fournisseurs de services appellent la fonction **FtgRegisterIdleRoutine** . Les paramètres d'entrée incluent une priorité facultative, un bloc de mémoire qui est transmis à votre fonction de rappel comme entrée, un délai à utiliser en quelque sorte et un ensemble d'indicateurs d'option. 
  
Les clients et les fournisseurs de services peuvent spécifier une priorité dans le paramètre _priIdle_ qui contrôle le mode d'exécution de la fonction Idle ou spécifier zéro si la priorité n'est pas un problème. Étant donné que les nombres négatifs représentent des priorités supérieures à ceux des nombres positifs ou zéro, des nombres négatifs doivent être attribués aux opérations de compression et de recherche. Les tâches qui se produisent une fois doivent recevoir des nombres positifs. 
  
Pour annuler l'inscription d'une fonction de rappel active, les clients et les fournisseurs de services appellent la fonction **DeregisterIdleRoutine** . Étant donné que **DeregisterIdleRoutine** opère de manière asynchrone, il est possible que la fonction de rappel soit appelée à tout moment pendant l'appel de désinscription, voire même après que **DeregisterIdleRoutine** a renvoyé. 
  
Pour modifier une partie ou la totalité des caractéristiques d'une fonction de rappel, les clients et les fournisseurs de services appellent la fonction **ChangeIdleRoutine** . **ChangeIdleRoutine** apporte des modifications en fonction de la définition du paramètre flags _ircIdle_ ; **ChangeIdleRoutine** peut modifier la fonction elle-même, sa priorité, son paramètre d'heure et son paramètre d'entrée. 
  
MAPI définit inactif de la même manière que le système d'exploitation, lorsque le système d'exploitation a une définition. Sur Win32, MAPI crée un thread avec une priorité de classe inactive pour planifier les tâches inactives. Cette thread effectue le suivi du temps et publie un message dans le thread qui doit exécuter la tâche inactive lorsque l'heure de son exécution arrive. Win32 planifie les threads, pas les processus. Si les tâches dont la priorité est supérieure à la priorité d'inactivité se produisent sur le poste de travail, la tâche inactive ne doit pas être planifiée pour l'exécution jusqu'à ce que les tâches soient terminées. 
  
Toutes les tâches inactives s'exécutent sur le thread qui a appelé **MAPIInitIdle**. MAPI dispose d'un thread distinct pour la planification, mais lorsqu'une tâche inactive devient éligible, il publie un message sur le thread d'initialisation et la tâche inactive est exécutée. Les implications pour les différents types de clients sont les suivantes.
  
|**Modèle de thread**|**Implique**|
|:-----|:-----|
|Thread unique  <br/> |Pas de problème. Les fonctions inActives s'exécutent sur le thread principal de votre client et sont sérialisées via la boucle de message.  <br/> |
|Thread libre  <br/> |Les fonctions inActives doivent être thread-safe, mais votre client dispose déjà de l'infrastructure nécessaire. Il se peut que votre client n'ait pas du tout besoin du moteur inactif MAPI.  <br/> |
|Thread cloisonné  <br/> |La fonction Idle doit s'exécuter sur le même thread qui l'a inscrite si elle veut utiliser MAPI, OLE ou toute autre interface COM. La méthode la plus simple consiste à enregistrer une fonction inactive avec MAPI qui publie un message vers le thread approprié et de distribuer la fonction inactive «Real» directement à partir de la boucle de message de ce thread.  <br/> |
   

