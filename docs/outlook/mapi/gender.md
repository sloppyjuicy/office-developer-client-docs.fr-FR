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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428647"
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

