---
title: Moteur MAPI inactif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f587b5785cda8d61c437976b3cf3a6a00e768813
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461439"
---
# <a name="mapi-idle-engine"></a>Moteur MAPI inactif

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit plusieurs fonctions qui sont collectivement appelées moteur inactif. Ces fonctions permettent aux clients, aux fournisseurs de carnets d’adresses et aux fournisseurs de magasins de messages d’effectuer diverses tâches pendant les périodes lentes de la session ou en réponse à un temps lent. Par exemple, les clients et les fournisseurs de services peuvent différer les opérations lentes ou fermer des fichiers qui sont restés inutilisés pendant une longue période. Les fournisseurs de transport n’utilisent généralement pas le moteur inactif, car la méthode **IXPLogon::Idle** prend sa place. Pour plus d’informations, [voir IXPLogon::Idle](ixplogon-idle.md).
  
Pour utiliser le moteur inactif, les clients et les fournisseurs de services créent une fonction de rappel qui contient les tâches qui doivent se produire lorsque le sous-système MAPI est inactif. Lorsque MAPI détecte le temps d’inactivité, il appelle cette fonction de rappel. La fonction de rappel suit le prototype **FNIDLE** , défini comme suit : 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Pour plus d’informations, [voir FNIDLE](fnidle.md).
  
Les fonctions qui font le moteur inactif sont :
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Pour inscrire une fonction de rappel, les clients et les fournisseurs de services appellent la **fonction FtgRegisterIdleRoutine** . Les paramètres d’entrée incluent une priorité facultative, un bloc de mémoire transmis à votre fonction de rappel en tant qu’entrée, une durée d’utilisation appropriée et un ensemble d’indicateurs d’option. 
  
Les clients et les fournisseurs de services peuvent spécifier une priorité dans le paramètre _priIdle_ qui contrôle le fonctionnement de la fonction inactive ou spécifier zéro si la priorité n’est pas un problème. Étant donné que les nombres négatifs représentent des priorités plus élevées que les nombres positifs ou zéro, les opérations de compression et de recherche doivent être affectées à des nombres négatifs. Les tâches qui se produisent une seule fois doivent se faire attribuer des nombres positifs. 
  
Pour désinsister une fonction de rappel active, les clients et les fournisseurs de services appellent la **fonction DeregisterIdleRoutine** . Étant donné que **DeregisterIdleRoutine** fonctionne de manière asynchrone, il est possible que la fonction de rappel soit invoquée à tout moment pendant l’appel de suppression d’register et même après le retour de **DeregisterIdleRoutine** . 
  
Pour modifier une partie ou l’ensemble des caractéristiques d’une fonction de rappel, les clients et les fournisseurs de services appellent la **fonction ChangeIdleRoutine** . **ChangeIdleRoutine** effectue des modifications en fonction de la façon dont le paramètre  _d’indicateurs est_ paramétré ; **ChangeIdleRoutine peut** modifier la fonction elle-même, sa priorité, son paramètre d’heure et son paramètre d’entrée. 
  
MAPI définit inactif de la même manière que le système d’exploitation, lorsque le système d’exploitation possède une définition. Sur Win32, MAPI crée un thread avec une priorité de classe inactive pour planifier les tâches inactives. Ce thread effectue le suivi de l’heure et publie un message dans le thread qui consiste à exécuter la tâche inactive lorsque le moment de son exécution arrive. Win32 programme les threads, et non les processus. Si des tâches dont la priorité est supérieure à la priorité d’inactivité se produisent sur la station de travail, la tâche inactive ne doit pas être programmée pour l’exécution tant que les tâches n’ont pas été terminées. 
  
Toutes les tâches inactives s’exécutent sur le thread qui a **appelé MAPIInitIdle**. MAPI dispose d’un thread distinct pour la planification, mais lorsqu’une tâche inactive devient éligible, elle publie un message sur le thread d’initialisation et la tâche inactive y est exécutée. Les implications pour les différents types de clients sont les suivantes.
  
|**Modèle de thread**|**Implication**|
|:-----|:-----|
|Thread unique  <br/> |Pas de problème. Les fonctions inactives s’exécutent sur le thread principal de votre client et sont sérialisées via la boucle de message.  <br/> |
|Thread libre  <br/> |Les fonctions inactives doivent être thread-safe, mais votre client dispose déjà de l’infrastructure nécessaire. Votre client n’a peut-être pas besoin du moteur d’inactivité MAPI.  <br/> |
|Threads de threads de location  <br/> |La fonction inactive doit s’exécuter sur le thread qui l’a inscrite si elle souhaite utiliser MAPI, OLE ou toute autre interface COM. La manière la plus simple consiste à inscrire une fonction inactive avec MAPI qui publie un message sur le thread de droite et répartit la fonction inactive « réelle » directement à partir de la boucle de messages de ce thread.  <br/> |
   

