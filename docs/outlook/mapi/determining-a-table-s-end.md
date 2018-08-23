---
title: Définition de la fin d’un tableau
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f9979baf144b6106adcec416ee04439404e05d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576343"
---
# <a name="determining-a-tables-end"></a>Définition de la fin d’un tableau

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Une erreur fréquente consiste à supposent que la fin de la table a été atteinte lorsque : 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) a été appelée dans une boucle, à la fin de la boucle déterminée par le nombre de lignes renvoyé par [IMAPITable::GetRowCount](imapitable-getrowcount.md). Le nombre **GetRowCount** renvoie ne représente pas toujours le nombre exact de lignes de la table ; Il s’agit d’un nombre approximatif. 
    
- **QueryRows** a été appelée avec un nombre défini de lignes et moins de lignes sont renvoyées. Il est pas **QueryRows** retourne une ligne avec un nombre de lignes égal à zéro qu’il n’y a plus aucune ligne à récupérer. 
    
> [!IMPORTANT]
> La seule fois où un appelant peut supposer que le curseur est positionné à la fin de la table pour un nombre positif de lignes ou au début de la table pour un nombre de lignes négatif est lorsque la valeur S_OK et aucune ligne est renvoyés. La valeur MAPI_E_NOT_FOUND n’est jamais retourné. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

