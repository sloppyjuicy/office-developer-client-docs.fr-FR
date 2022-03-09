---
title: Détermination de la fin d’une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
ms.openlocfilehash: 390a786a323a28ae3549f174edfabc2d549e7ed2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373731"
---
# <a name="determining-a-tables-end"></a>Détermination de la fin d’une table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Une erreur courante consiste à supposer que la fin du tableau a été atteinte dans les cas suivants : 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) a été appelé dans une boucle, avec la fin de la boucle déterminée par le nombre de lignes renvoyé par [IMAPITable::GetRowCount](imapitable-getrowcount.md). Le nombre que **GetRowCount renvoie** ne représente pas toujours le nombre exact de lignes dans le tableau ; il s’agit d’un nombre approximatif. 
    
- **QueryRows a** été appelé avec un nombre fixe de lignes et moins de lignes sont renvoyées. Ce n’est qu’après que **QueryRows** renvoie un jeu de lignes avec un nombre de lignes égal à zéro qu’il n’y a plus de lignes à récupérer. 
    
> [!IMPORTANT]
> La seule fois qu’un appelant peut supposer que le curseur est positionné à la fin du tableau pour un nombre de lignes positif ou au début du tableau pour un nombre de lignes négatif, c’est lorsque la valeur S_OK et zéro lignes sont renvoyées. La valeur MAPI_E_NOT_FOUND n’est jamais renvoyée. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

