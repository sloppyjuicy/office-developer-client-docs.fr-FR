---
title: Déterminer la fin d’une Table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783156"
---
# <a name="determining-a-tables-end"></a>Déterminer la fin d’une Table

  
  
**S’applique à**: Outlook 
  
 Une erreur fréquente consiste à supposent que la fin de la table a été atteinte lorsque : 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) a été appelée dans une boucle, à la fin de la boucle déterminée par le nombre de lignes renvoyé par [IMAPITable::GetRowCount](imapitable-getrowcount.md). Le nombre **GetRowCount** renvoie ne représente pas toujours le nombre exact de lignes de la table ; Il s’agit d’un nombre approximatif. 
    
- **QueryRows** a été appelée avec un nombre défini de lignes et moins de lignes sont renvoyées. Il est pas **QueryRows** retourne une ligne avec un nombre de lignes égal à zéro qu’il n’y a plus aucune ligne à récupérer. 
    
> [!IMPORTANT]
> La seule fois où un appelant peut supposer que le curseur est positionné à la fin de la table pour un nombre positif de lignes ou au début de la table pour un nombre de lignes négatif est lorsque la valeur S_OK et aucune ligne est renvoyés. La valeur MAPI_E_NOT_FOUND n’est jamais retourné. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

