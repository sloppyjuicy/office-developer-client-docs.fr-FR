---
title: Moteur inactif MAPI
description: Fournit une vue d’ensemble détaillée du moteur inactif MAPI et fournit des liens vers les fonctions du moteur inactif.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
ms.openlocfilehash: 370d155de99e2ba791300914dfe4081a5567dc06
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817829"
---
# <a name="mapi-idle-engine"></a>Moteur inactif MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit plusieurs fonctions qui sont collectivement appelées moteur inactif. Ces fonctions permettent aux clients, aux fournisseurs de carnets d’adresses et aux fournisseurs de magasins de messages d’effectuer différentes tâches pendant les temps lents de la session ou en réponse à un temps lent. Par exemple, les clients et les fournisseurs de services peuvent différer les opérations lentes ou fermer les fichiers qui sont restés inutilisés pendant une longue période. Les fournisseurs de transport n’utilisent généralement pas le moteur inactif, car la méthode **IXPLogon::Idle** prend sa place. Pour plus d’informations, consultez [IXPLogon::Idle](ixplogon-idle.md).
  
Pour utiliser le moteur inactif, les clients et les fournisseurs de services créent une fonction de rappel qui contient les tâches qui doivent se produire lorsque le sous-système MAPI est inactif. Lorsque MAPI détecte le temps d’inactivité, il appelle cette fonction de rappel. La fonction de rappel suit le prototype **FNIDLE** , défini comme suit : 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Pour plus d’informations, consultez [FNIDLE](fnidle.md).
  
Les fonctions qui composent le moteur inactif sont les suivantes :
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Pour inscrire une fonction de rappel, les clients et les fournisseurs de services appellent la fonction **FtgRegisterIdleRoutine** . Les paramètres d’entrée incluent une priorité facultative, un bloc de mémoire passé à votre fonction de rappel en tant qu’entrée, une durée d’utilisation appropriée et un ensemble d’indicateurs d’option. 
  
Les clients et les fournisseurs de services peuvent spécifier une priorité dans le paramètre _priIdle_ qui contrôle la façon dont la fonction inactive s’exécute ou spécifiez zéro si la priorité n’est pas un problème. Étant donné que les nombres négatifs représentent des priorités plus élevées que les nombres positifs ou zéro, les opérations de compression et de recherche doivent se faire attribuer des nombres négatifs. Les tâches qui se produisent une fois doivent être affectées à des nombres positifs. 
  
Pour désinscrire une fonction de rappel active, les clients et les fournisseurs de services appellent la fonction **DeregisterIdleRoutine** . Étant donné que **DeregisterIdleRoutine** fonctionne de façon asynchrone, il est possible d’appeler la fonction de rappel à tout moment pendant l’appel de désinscription et éventuellement même après le retour de **DeregisterIdleRoutine** . 
  
Pour modifier une partie ou l’ensemble des caractéristiques d’une fonction de rappel, les clients et les fournisseurs de services appellent la fonction **ChangeIdleRoutine** . **ChangeIdleRoutine** apporte des modifications en fonction de la façon dont le paramètre  _d’indicateur ircIdle_ est défini ; **ChangeIdleRoutine** peut modifier la fonction elle-même, sa priorité, son paramètre d’heure et son paramètre d’entrée. 
  
MAPI définit l’inactivité de la même manière que le système d’exploitation, lorsque le système d’exploitation a une définition. Sur Win32, MAPI crée un thread avec une priorité de classe inactive pour planifier des tâches inactives. Ce thread effectue le suivi de l’heure et publie un message au thread qui consiste à exécuter la tâche inactive lorsque l’heure de son exécution arrive. Win32 planifie les threads, pas les processus. Si des tâches dont la priorité est supérieure à la priorité d’inactivité se produisent sur la station de travail, la tâche inactive ne doit pas être planifiée pour l’exécution tant que les tâches ne sont pas terminées. 
  
Toutes les tâches inactives s’exécutent sur le thread qui a appelé **MAPIInitIdle**. MAPI dispose d’un thread distinct pour la planification, mais lorsqu’une tâche inactive devient éligible, il publie un message vers le thread d’initialisation et la tâche inactive y est exécutée. Les implications pour différents types de clients sont les suivantes.
  
|**Modèle de thread**|**Implication**|
|:-----|:-----|
|Monothread  <br/> |Pas de problème. Les fonctions inactives s’exécutent sur le thread principal de votre client et sont sérialisées via la boucle de message. |
|Thread libre  <br/> |Les fonctions inactives doivent être thread-safe, mais votre client dispose déjà de l’infrastructure nécessaire. Votre client n’a peut-être pas besoin du moteur inactif MAPI. |
|Threads d’appartement  <br/> |La fonction inactive doit s’exécuter sur le même thread que celui qui l’a inscrite si elle souhaite utiliser MAPI, OLE ou toute autre interface COM. La méthode la plus simple consiste à inscrire une fonction inactive auprès de MAPI qui publie un message sur le thread approprié et distribue la fonction inactive « réelle » directement à partir de la boucle de message de ce thread. |
   

