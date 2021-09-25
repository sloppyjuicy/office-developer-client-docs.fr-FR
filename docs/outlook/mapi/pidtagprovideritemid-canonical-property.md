---
title: Propriété canonique PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d69ff57fd02a6f25e97c24360519f3c215b731e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574859"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propriété canonique PidTagProviderItemId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un identificateur pour un dossier ou un élément dans une boutique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Identificateur :  <br/> |0x0EA3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un dossier ou un élément, mais doivent conserver la même valeur entre les sessions. Les fournisseurs du Store utilisent cette propriété pour identifier les résultats de recherche renvoyés par un moteur de recherche.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

