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
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428983"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Regroupement et limitation des tables dans les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes permettent souvent aux utilisateurs de contrôler le mode d'affichage du contenu d'un dossier. En règle générale, un utilisateur peut choisir de regrouper les messages en fonction de la valeur d'une ou plusieurs propriétés de message ou choisir d'exclure les messages qui répondent à certains critères. Cette opération est réalisée à l'aide de l'interface [IMAP: IUnknown](imapitableiunknown.md) . Les applications clientes peuvent restreindre les lignes renvoyées par la table à tous les critères spécifiés par l'utilisateur. Par conséquent, un fournisseur de banque de messages doit implémenter les méthodes **IMAPITable** suivantes. 
  
|IMAPITable * * méthode * *|**Description**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Renvoie les lignes de tableau qui correspondent aux critères spécifiés.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie le jeu de colonnes d'un tableau ou l'ensemble des colonnes actuellement utilisées.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d'une table, en commençant à partir d'une position donnée.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Applique une restriction à un tableau de sorte que les appels ultérieurs à **FindRow** renvoient uniquement les lignes correspondant à la restriction.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Spécifie les colonnes qui doivent être renvoyées lorsque les lignes sont extraites de la table.  <br/> |
   
Les restrictions peuvent être complexes à implémenter; Pour plus d'informations, consultez la rubrique [à propos des restrictions](about-restrictions.md). Pour plus d'informations sur l'implémentation des tables, voir [MAPI tables](mapi-tables.md).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

