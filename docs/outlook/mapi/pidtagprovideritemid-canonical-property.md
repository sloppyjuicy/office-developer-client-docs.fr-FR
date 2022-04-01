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
description: Spécifie un identificateur pour un dossier ou un élément dans une boutique. Les fournisseurs du Store utilisent cette propriété pour identifier les résultats de recherche renvoyés par un moteur de recherche.
ms.openlocfilehash: f489576188d9ec5be7158743a22ad171d4dbe485
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523830"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propriété canonique PidTagProviderItemId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un identificateur pour un dossier ou un élément dans une boutique.
  
|Propriété |Valeur |
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

