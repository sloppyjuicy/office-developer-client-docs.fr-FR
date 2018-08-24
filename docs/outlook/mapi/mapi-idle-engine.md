---
title: Moteur d’inactivité MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9fdc254053c2d35c83866bd8a076279fd383db02
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583035"
---
# <a name="mapi-idle-engine"></a>Moteur d’inactivité MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI offre plusieurs fonctions qui constituent le moteur inactif. Ces fonctions permettent de clients, fournisseurs de carnet d’adresses et les fournisseurs de banque de messages effectuer diverses tâches pendant les heures de lentes dans la session ou en réponse à un moment lent. Par exemple, clients et fournisseurs de services peuvent différer des opérations lentes ou fermer les fichiers qui sont restés inutilisés pendant une longue période. Généralement, les fournisseurs de transport n’utilisent pas du moteur inactif, car la méthode **IXPLogon::Idle** prend sa place. Pour plus d’informations, voir [IXPLogon::Idle](ixplogon-idle.md).
  
Pour utiliser le moteur d’inactivité, clients et fournisseurs de services de créer une fonction de rappel qui contient les tâches qui doivent se produire lorsque le sous-système MAPI est inactif. Lorsque MAPI détecte la durée d’inactivité, il appelle cette fonction de rappel. La fonction de rappel suit le prototype **FNIDLE** , défini comme suit : 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Pour plus d’informations, voir [FNIDLE](fnidle.md).
  
Les fonctions qui constituent le moteur inactif sont les suivants :
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Pour enregistrer une fonction de rappel, clients et fournisseurs de services d’appel la fonction **FtgRegisterIdleRoutine** . Les paramètres d’entrée sont une priorité facultative, un bloc de mémoire est passée à la fonction de rappel comme entrée, un laps de temps à utiliser en aucune manière appropriée, et un ensemble de l’option indicateurs. 
  
Clients et fournisseurs de services peuvent spécifier une priorité dans le paramètre _priIdle_ qui contrôle le fonctionne de la fonction inactive ou zéro si la priorité n’est pas un problème. Étant donné que les nombres négatifs représentent une priorité supérieure à zéro ou à des nombres positifs, les opérations de recherche et la compression doivent être affectées à des nombres négatifs. Les tâches qui se produisent une fois doivent être assignées à des nombres positifs. 
  
Pour annuler l’enregistrement d’une fonction de rappel active, clients et fournisseurs de services appellent la fonction **DeregisterIdleRoutine** . **DeregisterIdleRoutine** fonctionne de manière asynchrone, il est possible de la fonction de rappel à appeler à tout moment pendant l’appel d’annuler l’enregistrement et peut-être même une fois que **DeregisterIdleRoutine** a renvoyé. 
  
Pour modifier certaines ou toutes les caractéristiques d’une fonction de rappel, clients et fournisseurs de services appellent la fonction **ChangeIdleRoutine** . **ChangeIdleRoutine** apporte les modifications en fonction du paramétrage de du paramètre flags _ircIdle_ ; **ChangeIdleRoutine** peut modifier la fonction elle-même, sa priorité, paramètre de l’heure et paramètre d’entrée. 
  
MAPI définit inactif le même que le système d’exploitation, lorsque le système d’exploitation dispose d’une définition. Win32, MAPI crée un thread de priorité classe inactif pour planifier les tâches inactives. Ce thread effectue le suivi de l’heure et publie un message au thread qui doit exécuter la tâche d’inactivité de l’heure de son exécution. Win32 planifie des threads, ne traite pas. Si les tâches qui ont une priorité plus élevée que celle inactif sont produisent sur la station de travail, la tâche d’inactivité ne doit pas obtenir planifiée pour l’exécution tant que les tâches sont terminées. 
  
Toutes les tâches inactives exécutées sur le thread qui a appelé **MAPIInitIdle**. MAPI a un thread distinct pour la planification, mais lorsqu’une tâche d’inactivité devient éligible, il publie un message renvoyé sur le thread d’initialisation et de la tâche d’inactivité est exécutée. Les implications des différents types de clients sont les suivants :
  
|**Modèle de thread**|**Implication**|
|:-----|:-----|
|Un seul thread  <br/> |Pas de problème. Fonctions inactives s’exécuter sur le thread principal de votre client et sont sérialisées par le biais de la boucle de message.  <br/> |
|Libre de thread  <br/> |Fonctions inactives doivent être thread-safe, mais votre client a déjà l’infrastructure nécessaire. Votre client n’ayez pas du tout le moteur inactif MAPI.  <br/> |
|Cloisonnement sans thread  <br/> |Fonction inactive doit s’exécuter sur le même thread qui a enregistré s’il souhaite utiliser toutes les autres interfaces COM, OLE ou MAPI. La façon la plus simple consiste à enregistrer une fonction inactive MAPI qui publie un message au thread droite et distribuer la fonction « en » inactive directement à partir de la boucle de message de ce thread.  <br/> |
   

