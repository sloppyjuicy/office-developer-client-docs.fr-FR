---
title: Conseils pour améliorer les performances de table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787353"
---
# <a name="tips-for-better-table-performance"></a>Conseils pour améliorer les performances de table
  
**S’applique à**: Outlook 
  
Étant donné que de nombreuses opérations de table peuvent prendre du temps et il n’existe aucun moyen d’indiquer la progression, il est utile d’utiliser les techniques suivantes pour améliorer les performances :
  
- **Rendre [IMAPITable : IUnknown](imapitableiunknown.md) appelle dans l’ordre correct**
    
   Clients et fournisseurs de services peuvent travailler avec des tableaux de diverses façons. Ils peuvent ouvrir la table et récupérer les données pour toutes les lignes à l’aide de l’ensemble de colonnes par défaut et l’ordre de tri. Ils peuvent également modifier cet affichage par défaut de la table en modifiant l’ensemble de colonnes, modification de l’ordre de tri ou en établissant une restriction pour limiter l’étendue de la table. Les utilisateurs de tableau que vous souhaitez effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent effectuer les dans l’ordre suivant :
    
    1. Définir une colonne avec [IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Établir une restriction avec [IMAPITable](imapitable-restrict.md).
        
    3. Définir un ordre de tri avec [IMAPITable::SortTable](imapitable-sorttable.md).
    
    Exécution de ces tâches dans l’ordre suivant limite le nombre de lignes et de colonnes qui seront triées, ce qui améliore les performances.
    
- **Délai d’une opération à l’aide de l’indicateur TBL_BATCH si possible**
    
    Définition de la table\_indicateur de lot sur une méthode permet à l’implémentation de tableau collecter plusieurs appels avant de traiter sur n’importe lequel d'entre eux. Au lieu de passer des appels nombreux à un serveur distant. une implémentation de table, permettent d’effectuer toutes les opérations en même temps. Les résultats des opérations ne sont pas évaluées jusqu'à ce qu’ils ne sont pas nécessaires. 
    
    Par exemple, lorsqu’un client appelle [IMAPITable](imapitable-restrict.md) pour spécifier une restriction avec la TBL\_lot indicateur défini, la restriction n’avez pas à entrent en vigueur jusqu'à ce que le client appelle [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données. Ainsi, l’implémentation de table combiner le travail de deux appels en une seule. Les utilisateurs qui tirent parti de la table de table\_indicateur lot Sachez que gestion dans ces conditions d’erreur peut être plus complexe. 
    
    Étant donné que la gestion des erreurs à partir d’une opération différée sont similaire à la gestion des erreurs lors de l’interface MAPI\_DEFERRED_ERRORS est défini, voir [Report des erreurs MAPI](deferring-mapi-errors.md) pour plus d’informations. 
    
- **Conserver un cache des propriétés couramment utilisées**
    
    Fournisseurs de services de mise en œuvre de tables peuvent réduire le temps que nécessaire pour créer un affichage en mettant en cache les copies des propriétés de l’objet couramment utilisés. Conserver une copie de ces propriétés en mémoire enregistre avoir à récupérer à partir de l’objet chaque fois que l’affichage doit être reconstruite.
    
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

