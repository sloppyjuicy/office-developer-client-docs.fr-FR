---
title: Conseils pour améliorer les performances d’une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412512"
---
# <a name="tips-for-better-table-performance"></a>Conseils pour améliorer les performances d’une table
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que de nombreuses opérations de table peuvent prendre du temps et qu’il n’existe aucun moyen d’indiquer la progression, il est utile d’utiliser les techniques suivantes pour améliorer les performances :
  
- **Effectuer [des appels IMAPITable : IUnknown](imapitableiunknown.md) dans l’ordre correct**
    
   Les clients et les fournisseurs de services peuvent utiliser des tableaux de différentes manières. Ils peuvent ouvrir la table et récupérer les données de toutes les lignes à l’aide de l’ordre de tri et du jeu de colonnes par défaut. Ils peuvent également modifier cet affichage par défaut du tableau en modifiant le jeu de colonnes, en modifiant l’ordre de tri ou en établissant une restriction pour affiner l’étendue du tableau. Les utilisateurs de tableau qui ont l’intention d’effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent les effectuer dans l’ordre suivant :
    
    1. Définissez un ensemble de colonnes [avec IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Établir une restriction avec [IMAPITable::Restrict](imapitable-restrict.md).
        
    3. Définissez un ordre de tri [avec IMAPITable::SortTable](imapitable-sorttable.md).
    
    L’exécution de ces tâches dans cet ordre limite le nombre de lignes et de colonnes qui seront triées, améliorant ainsi les performances.
    
- **Retarder une opération à l’aide de l’TBL_BATCH si possible**
    
    La définition de l’indicateur BATCH TBL sur une méthode permet à l’implémenteur de table de collecter plusieurs appels avant d’agir \_ sur l’un d’eux. Au lieu d’effectuer potentiellement de nombreux appels vers un serveur distant ; un implémenteur de table peut en effectuer une, en effectuer toutes les opérations en même temps. Les résultats des opérations ne sont pas évalués tant qu’ils ne sont pas nécessaires. 
    
    Par exemple, lorsqu’un client appelle [IMAPITable::Restrict](imapitable-restrict.md) pour spécifier une restriction avec l’indicateur BATCH TBL, la restriction n’a pas besoin d’entrer en vigueur tant que le client n’appelle \_ [pas IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données. Cela permet à l’implémenteur de table de combiner le travail de deux appels en un seul. Les utilisateurs de tableau qui tirez parti de l’indicateur BATCH TBL doivent savoir que la gestion des erreurs dans ces \_ conditions peut être plus complexe. 
    
    Étant donné que la gestion des erreurs à partir d’une opération différée est similaire à la gestion des erreurs lorsque l’indicateur DEFERRED_ERRORS MAPI est définie, voir Différer les erreurs MAPI pour plus \_ d’informations. [](deferring-mapi-errors.md) 
    
- **Conserver un cache des propriétés couramment utilisées**
    
    Les fournisseurs de services qui implémentent des tables peuvent réduire le temps qu’il faut pour créer un affichage en mettant en cache des copies des propriétés d’objet couramment utilisées. Conserver une copie de ces propriétés en mémoire permet d’éviter de devoir les récupérer à partir de l’objet chaque fois que l’affichage doit être reconstruit.
    
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

