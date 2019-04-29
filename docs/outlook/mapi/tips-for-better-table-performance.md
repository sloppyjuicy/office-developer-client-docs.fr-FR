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
  
Étant donné que de nombreuses opérations de table peuvent prendre du temps et qu'il n'existe aucun moyen d'indiquer la progression, il est utile d'utiliser les techniques suivantes pour améliorer les performances:
  
- **Créer une fonction [IMAPITable: appels IUnknown](imapitableiunknown.md) dans le bon ordre**
    
   Les clients et les fournisseurs de services peuvent travailler avec des tableaux de différentes façons. Ils peuvent ouvrir le tableau et extraire les données de toutes les lignes à l'aide du jeu de colonnes et de l'ordre de tri par défaut. Ils peuvent également modifier cette vue par défaut du tableau en modifiant le jeu de colonnes, en modifiant l'ordre de tri ou en établissant une restriction pour limiter l'étendue de la table. Les utilisateurs de tableau qui envisagent d'effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent les exécuter dans l'ordre suivant:
    
    1. Définissez un jeu de colonnes avec l'aide de la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md).
        
    2. Établissez une restriction avec la fonction [IMAPITable:: Restrict](imapitable-restrict.md).
        
    3. Définissez un ordre de tri à l'aide de la fonction [IMAPITable:: SortTable](imapitable-sorttable.md).
    
    L'exécution de ces tâches dans cet ordre limite le nombre de lignes et de colonnes qui seront triées, ce qui améliore les performances.
    
- **ReTarder une opération à l'aide de l'indicateur TBL_BATCH dans la mesure du possible**
    
    La définition de\_l'indicateur de lot de tbl sur une méthode permet à l'implémenteur de table de collecter plusieurs appels avant d'agir sur l'un d'eux. Au lieu de passer un grand nombre d'appels à un serveur distant; un implémenteur de tableau peut en créer un, ce qui effectue toutes les opérations à la fois. Les résultats des opérations ne sont pas évalués tant qu'ils ne sont pas nécessaires. 
    
    Par exemple, lorsqu'un client appelle [IMAPITable:: Restrict](imapitable-restrict.md) pour spécifier une restriction avec l'\_indicateur de lot tbl défini, la restriction n'a pas besoin de prendre effet tant que le client n'appelle pas [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer les données. Cela permet à l'implémenteur de tableau de combiner le travail de deux appels en un seul. Les utilisateurs de tableau qui tirent parti\_de l'indicateur de lot tbl doivent savoir que la gestion des erreurs dans ces conditions peut être plus complexe. 
    
    Étant donné que la gestion des erreurs à partir d'une opération différée est similaire à\_la gestion des erreurs lors de la définition de l'indicateur MAPI DEFERRED_ERRORS, reportez-vous à la rubrique [Report des erreurs MAPI](deferring-mapi-errors.md) pour plus d'informations. 
    
- **Conserver un cache des propriétés couramment utilisées**
    
    Les fournisseurs de services qui implémentent des tables peuvent réduire le temps nécessaire pour créer une vue en mettant en cache des copies des propriétés d'objets couramment utilisées. Conserver une copie de ces propriétés dans la mémoire permet aux utilisateurs de les récupérer à chaque régénération de l'affichage.
    
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

