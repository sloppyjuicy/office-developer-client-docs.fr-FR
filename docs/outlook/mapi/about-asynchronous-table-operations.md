---
title: Les opérations de table asynchrone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569420"
---
# <a name="about-asynchronous-table-operations"></a>Les opérations de table asynchrone
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’interface **IMAPITable** inclut trois méthodes qui fonctionnent de manière asynchrone et trois méthodes pour le contrôle d’une opération asynchrone. Le tableau suivant répertorie les méthodes suivantes : 
  
|**Opération asynchrone**|**Méthode de contrôle asynchrone**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Pour récupérer les informations d’état sur le type et l’opération en cours d’une table**
  
- Appelez [IMAPITable::GetStatus](imapitable-getstatus.md). Avec **GetStatus**, un utilisateur de la table peut déterminer si le tableau est statiques ou dynamiques, si une opération est en cours ou a terminé, et si une erreur s’est produite à partir d’une opération terminée. Par exemple, si un client a besoin d’annuler une opération de tri, car elle prend trop de temps, le client peut appeler tout d’abord **GetStatus** pour déterminer si, en fait, une opération de tri est actuellement de traitement. Ensuite, le client peut appeler [IMAPITable::Abort](imapitable-abort.md) pour l’arrêter. 
    
**Pour suspendre l’activité jusqu'à ce qu’une tâche asynchrone est terminée.**
  
- Appelez [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). L’appel **WaitForCompletion** permet la tâche se termine sans interruption. 
    
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

