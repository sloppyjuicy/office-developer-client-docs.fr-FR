---
title: Regroupement et restriction de tables dans les fournisseurs du Magasin de messages
description: Cet article décrit le regroupement et la restriction des tables dans les fournisseurs de magasins de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
ms.openlocfilehash: 72b8770ba7438e710ce821804aa866c6c0b4cba0
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816940"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Regroupement et restriction de tables dans les fournisseurs du Magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes permettent souvent aux utilisateurs de contrôler la façon dont le contenu d’un dossier est affiché. En règle générale, un utilisateur peut choisir de regrouper les messages en fonction de la valeur d’une ou plusieurs propriétés de message, ou peut choisir d’exclure les messages qui correspondent à certains critères. Pour ce faire, utilisez l’interface [IMAPITable : IUnknown](imapitableiunknown.md) . Les applications clientes peuvent limiter les lignes retournées à partir de la table aux critères spécifiés par l’utilisateur. Par conséquent, un fournisseur de magasin de messages doit implémenter les méthodes **IMAPITable** suivantes. 
  
|Méthode IMAPITable** **|**Description**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Retourne les lignes de table qui correspondent aux critères spécifiés. |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Retourne l’ensemble de colonnes dans une table ou l’ensemble de colonnes actuellement utilisées. |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Retourne une ou plusieurs lignes d’une table, en commençant à partir d’une position donnée. |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Applique une restriction à une table afin que les appels suivants à **FindRow** retournent uniquement les lignes qui correspondent à la restriction. |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Spécifie les colonnes à retourner lorsque des lignes sont récupérées à partir de la table. |
   
Les restrictions peuvent être complexes à implémenter; Pour plus d’informations, consultez [À propos des restrictions](about-restrictions.md). Pour plus d’informations sur l’implémentation de tables, consultez [Tables MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

