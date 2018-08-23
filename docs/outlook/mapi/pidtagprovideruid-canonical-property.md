---
title: Propriété canonique PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581054"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propriété canonique PidTagProviderUid

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une structure **MAPIUID** du fournisseur de services qui gère un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_UID  <br/> |
|Identificateur :  <br/> |0x300C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par tous les fournisseurs de services. Il contient une structure [MAPIUID](mapiuid.md) associée et généralement codée en dur par le fournisseur. Il est généralement utilisé par une application cliente qui intéresse dans uniquement les conteneurs de carnet d’adresse fournies par un fournisseur spécifique. 
  
Cette propriété s’affiche uniquement en tant qu’une entrée de la colonne dans la table fournisseur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

