---
title: Regroupement et limitation des tables dans les fournisseurs de banques de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec1c07a8d2c88680ebd94cf8ecd6901ed86ad100
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578786"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Regroupement et limitation des tables dans les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Applications clientes permettent souvent aux utilisateurs contrôler comment le contenu d’un dossier s’affiche. En règle générale, un utilisateur peut choisir que les messages regroupés en fonction de la valeur d’une ou plusieurs propriétés de message, ou peut choisir d’exclure les messages qui correspondent à certains critères. Cette opération est effectuée à l’aide de la [IMAPITable : IUnknown](imapitableiunknown.md) interface. Applications clientes peuvent restreindre les lignes renvoyées à partir de la table à l’utilisateur spécifie tous les critères. Par conséquent, un message stocker fournisseur doit implémenter les méthodes **IMAPITable** suivantes. 
  
|Méthode IMAPITable ** **|**Description**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Renvoie la table lignes qui correspondent aux critères spécifiés.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie l’ensemble de colonnes dans une table ou de l’ensemble des colonnes actuellement utilisées.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d’une table, à partir d’une position donnée.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Applique une restriction à une table de sorte que les appels suivants à **FindRow** retournent uniquement les lignes qui correspondent à la restriction.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Spécifie les colonnes qui doivent être retournés lorsque des lignes de la table.  <br/> |
   
Restrictions peuvent être complexes à implémenter ; Pour plus d’informations, voir [à propos des Restrictions](about-restrictions.md). Pour plus d’informations sur l’implémentation de tables, voir [Tables de MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

