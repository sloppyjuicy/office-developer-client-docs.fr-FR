---
title: Opérations des tables asynchrones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: Cet article fournit des informations sur les opérations de table asynchrones.
ms.openlocfilehash: f5dee48062281abf7f0f2b261e9ccddcb16c4ea9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816975"
---
# <a name="about-asynchronous-table-operations"></a>Opérations des tables asynchrones
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’interface **IMAPITable** comprend trois méthodes qui fonctionnent de façon asynchrone et trois méthodes pour contrôler une opération asynchrone. Le tableau suivant répertorie les méthodes suivantes : 
  
|**Opération asynchrone**|**Méthode de contrôle asynchrone**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Pour récupérer des informations d’état sur le type et l’opération en cours d’une table**
  
- Appelez [IMAPITable::GetStatus](imapitable-getstatus.md). Avec **GetStatus**, un utilisateur de table peut déterminer si la table est statique ou dynamique, si une opération est en cours ou est terminée, et si une erreur s’est produite à partir d’une opération terminée. Par exemple, si un client doit annuler une opération de tri parce qu’elle prend trop de temps, le client peut d’abord appeler **GetStatus** pour déterminer si, en fait, une opération de tri est en cours de traitement. Le client peut ensuite appeler [IMAPITable::Abort](imapitable-abort.md) pour l’arrêter. 
    
**Pour interrompre l’activité jusqu’à ce qu’une tâche asynchrone soit terminée**
  
- Appelez [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). L’appel de **WaitForCompletion** permet à la tâche de se terminer sans interruption. 
    
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

