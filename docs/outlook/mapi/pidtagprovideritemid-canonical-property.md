---
title: Propriété canonique PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 35a2d88ec838a9a76355ba6580e9cdbb3f28de56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786481"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propriété canonique PidTagProviderItemId

  
  
**S’applique à**: Outlook 
  
Spécifie un identificateur pour un dossier ou un élément dans une banque.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Identificateur :  <br/> |0x0EA3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Remarques

Fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un dossier ou un élément, mais doivent conserver la valeur de la même session. Fournisseurs de magasins d’utilisent cette propriété pour identifier des résultats de recherche renvoyés à partir d’un moteur de recherche.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

