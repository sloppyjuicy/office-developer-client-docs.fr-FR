---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786941"
---
# <a name="propid"></a>PROP_ID

  
  
**S’applique à**: Outlook 
  
Renvoie l’identificateur de propriété d’une balise de propriété spécifiée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> Balise de propriété qui contient l’identificateur à renvoyer.
    
## <a name="remarks"></a>Remarques

Chaque balise de propriété contient le type de propriété dans le mot de poids faible (bits 0 à 15) et l’identificateur de propriété dans le mot de poids fort (bits 16 à 31). La macro **PROP_ID** extrait l’identificateur de propriété et la place dans les bits 0 à 15 du nombre entier à renvoyer. Les bits restants de la valeur de retour sont définies sur zéro. 
  
La macro **PROP_ID** peut être utilisée, par exemple, pour récupérer un identificateur à transmettre à [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** récupère le nom de la propriété associé à un identificateur pour une propriété nommée. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros relatives aux Structures](macros-related-to-structures.md)

