---
title: Regroupement et restriction des tables dans les fournisseurs de magasins de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8698e3958a4cfbf4c7a358912a3ea9a760c4edb1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776647"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Regroupement et restriction des tables dans les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes permettent fréquemment aux utilisateurs de contrôler l’affichage du contenu d’un dossier. En règle générale, un utilisateur peut choisir de grouper des messages en fonction de la valeur d’une ou de plusieurs propriétés de message ou d’exclure les messages qui correspondent à certains critères. Pour ce faire, utilisez [l’interface IMAPITable : IUnknown](imapitableiunknown.md) . Les applications clientes peuvent limiter les lignes renvoyées à partir du tableau à tous les critères spécifiés par l’utilisateur. Par conséquent, un fournisseur de magasin de messages doit implémenter les méthodes **IMAPITable** suivantes. 
  
|Méthode IMAPITable** **|**Description**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Renvoie les lignes de tableau qui correspondent aux critères spécifiés. |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie l’ensemble des colonnes d’un tableau ou l’ensemble des colonnes actuellement utilisées. |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d’un tableau, à partir d’une position donnée. |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Applique une restriction à une table afin que les appels ultérieurs à **FindRow** retournent uniquement les lignes qui correspondent à la restriction. |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Spécifie les colonnes qui doivent être renvoyées lorsque des lignes sont extraites du tableau. |
   
Les restrictions peuvent être complexes à implémenter ; Pour plus d’informations, voir [À propos des restrictions](about-restrictions.md). Pour plus d’informations sur l’implémentation des tableaux, voir [Tableaux MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

