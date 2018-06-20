---
title: Regroupement et de restriction des tableaux dans les fournisseurs de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783418"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Regroupement et de restriction des tableaux dans les fournisseurs de banque de messages

  
  
**S’applique à**: Outlook 
  
Applications clientes permettent souvent aux utilisateurs contrôler comment le contenu d’un dossier s’affiche. En règle générale, un utilisateur peut choisir que les messages regroupés en fonction de la valeur d’une ou plusieurs propriétés de message, ou peut choisir d’exclure les messages qui correspondent à certains critères. Cette opération est effectuée à l’aide de la [IMAPITable : IUnknown](imapitableiunknown.md) interface. Applications clientes peuvent restreindre les lignes renvoyées à partir de la table à l’utilisateur spécifie tous les critères. Par conséquent, un message stocker fournisseur doit implémenter les méthodes **IMAPITable** suivantes. 
  
|Méthode IMAPITable ** **|**Description**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Renvoie la table lignes qui correspondent aux critères spécifiés.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie l’ensemble de colonnes dans une table ou de l’ensemble des colonnes actuellement utilisées.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d’une table, à partir d’une position donnée.  <br/> |
|[IMAPITable](imapitable-restrict.md) <br/> |Applique une restriction à une table de sorte que les appels suivants à **FindRow** retournent uniquement les lignes qui correspondent à la restriction.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Spécifie les colonnes qui doivent être retournés lorsque des lignes de la table.  <br/> |
   
Restrictions peuvent être complexes à implémenter ; Pour plus d’informations, voir [à propos des Restrictions](about-restrictions.md). Pour plus d’informations sur l’implémentation de tables, voir [Tables de MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

