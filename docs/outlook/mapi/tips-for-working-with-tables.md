---
title: Astuces pour l’working with Tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
ms.openlocfilehash: 09bfa569b660350023352611917559386a5a8293
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369552"
---
# <a name="tips-for-working-with-tables"></a>Astuces pour l’working with Tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Travailler avec une table MAPI est un peu comme une table de base de données relationnelle. Un utilisateur peut limiter le nombre de lignes et de colonnes dans l’affichage et spécifier son ordre. Les lignes peuvent être récupérées une par une ou par groupes. Un curseur qui assure le suivi de la position actuelle peut être déplacé vers un endroit spécifique du tableau. 
  
Pour utiliser des tables, les clients utilisent l’interface en lecture seule [IMAPITable : IUnknown](imapitableiunknown.md), tandis que les fournisseurs de services, selon qu’ils possèdent ou non les données sur la table, peuvent utiliser **IMAPITable** ou [ITableData : IUnknown](itabledataiunknown.md). Les opérations définies dans ces interfaces peuvent être classées en tant qu’opérations que tous les utilisateurs de tables font ou peuvent appeler et les opérations qui ne sont pas aussi largement utilisées, car elles sont plus avancées. Certaines opérations avancées sont plus complexes à implémenter . d’autres ne sont pas plus complexes, mais sont d’un intérêt pour une petite majorité de composants MAPI. 
  
Les opérations les plus courantes sont :
  
- Opérations de colonne, qui affectent des colonnes individuelles. Il s’agit notamment de spécifier les propriétés à inclure dans le jeu de colonnes et l’ordre dans lequel elles doivent être incluses.
    
- Opérations de ligne, qui affectent des lignes individuelles. Il s’agit notamment de la récupération des données et des opérations de maintenance : ajout, suppression et modification d’une ou plusieurs lignes.
    
- Opérations globales, qui affectent la table entière. Il s’agit notamment de la notification d’événement, de la recherche et du tri.
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

