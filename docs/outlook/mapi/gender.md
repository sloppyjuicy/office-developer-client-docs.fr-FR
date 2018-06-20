---
title: Sexe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783400"
---
# <a name="gender"></a>Sexe

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

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

