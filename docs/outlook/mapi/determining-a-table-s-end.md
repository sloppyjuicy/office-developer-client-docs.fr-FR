---
title: Détermination de la fin d'une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420086"
---
# <a name="determining-a-tables-end"></a>Détermination de la fin d'une table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Une erreur courante consiste à supposer que la fin de la table a été atteinte dans les cas suivants: 
  
- [IMAPITable:: QueryRows](imapitable-queryrows.md) a été appelé dans une boucle, avec la fin de la boucle déterminée par le nombre de lignes renvoyé par la méthode [IMAPITable:: GetRowCount](imapitable-getrowcount.md). Le nombre renvoyé par **GetRowCount** ne représente pas toujours le nombre exact de lignes dans le tableau; Il s'agit d'un nombre approximatif. 
    
- **QueryRows** a été appelé avec un nombre fixe de lignes et moins de lignes sont renvoyées. Il n'est pas jusqu'à ce que **QueryRows** renvoie un jeu de lignes dont le nombre de lignes est égal à zéro, il n'y a plus de lignes à récupérer. 
    
> [!IMPORTANT]
> Le seul moment où un appelant peut supposer que le curseur est positionné à la fin de la table pour un nombre positif de lignes ou au début de la table pour un nombre de lignes négatif est lorsque la valeur S_OK et zéro ligne sont renvoyées. La valeur MAPI_E_NOT_FOUND n'est jamais renvoyée. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

