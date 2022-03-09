---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
ms.openlocfilehash: 26b1c76055d405b2ad6142112fc78147964b702c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376902"
---
# <a name="gender"></a>Gender

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les valeurs possibles pour le sexe d’un utilisateur de messagerie.
  
## <a name="quick-info"></a>Informations rapides

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>Membres

 _genderMin_
  
> Nombre minimal de valeurs différentes pris en charge pour le sexe.
    
 _genderUnspecified_
  
> Le sexe n’est pas spécifié pour l’utilisateur de messagerie.
    
 _genderFemale_
  
> L’utilisateur de messagerie est une femme.
    
 _genderMale_
  
> L’utilisateur de messagerie est un homme.
    
 _genderCount_
  
> Nombre de valeurs différentes prise en charge pour le sexe.
    
 _genderMax_
  
> Nombre maximal de valeurs différentes pris en charge pour le sexe.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagGender](pidtaggender-canonical-property.md)

