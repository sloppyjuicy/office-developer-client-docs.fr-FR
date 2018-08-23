---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588453"
---
# <a name="gender"></a>Gender

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie les valeurs possibles pour le genre d’un utilisateur de messagerie.
  
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

## <a name="members"></a>Members

 _genderMin_
  
> Le nombre minimal de différentes valeurs de prise en charge pour le sexe.
    
 _genderUnspecified_
  
> Le sexe n’est pas spécifié pour l’utilisateur de messagerie.
    
 _genderFemale_
  
> L’utilisateur de messagerie est féminin.
    
 _genderMale_
  
> L’utilisateur de messagerie est masculin.
    
 _genderCount_
  
> Le nombre de valeurs différentes pris en charge pour le sexe.
    
 _genderMax_
  
> Le nombre maximal de valeurs différentes pris en charge pour le sexe.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagGender](pidtaggender-canonical-property.md)

