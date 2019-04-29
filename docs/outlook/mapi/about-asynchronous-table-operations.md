---
title: Opérations des tables asynchrones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439568"
---
# <a name="about-asynchronous-table-operations"></a>Opérations des tables asynchrones
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'interface **IMAPITable** comprend trois méthodes qui fonctionnent de manière asynchrone et trois méthodes pour contrôler une opération asynchrone. Le tableau suivant répertorie ces méthodes: 
  
|**Opération asynchrone**|**Méthode de contrôle asynchrone**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Pour récupérer des informations d'État sur le type et l'opération en cours d'une table**
  
- Appeler [IMAPITable:: GetStatus](imapitable-getstatus.md). Avec **GetStatus**, un utilisateur de tableau peut déterminer si la table est statique ou dynamique, si une opération est en cours ou est terminée, et si une erreur s'est produite à partir d'une opération terminée. Par exemple, si un client a besoin d'annuler une opération de tri parce qu'il prend trop de temps, le client peut tout d'abord appeler **GetStatus** pour déterminer si une opération de tri est actuellement en cours de traitement. Le client peut alors appeler [IMAPITable:: Abort](imapitable-abort.md) pour l'arrêter. 
    
**Pour suspendre l'activité jusqu'à la fin d'une tâche asynchrone**
  
- Appeler [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md). L'appel de **WaitForCompletion** permet à la tâche de se terminer sans interruption. 
    
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

