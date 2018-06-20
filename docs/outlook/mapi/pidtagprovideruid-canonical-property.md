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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786458"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propriété canonique PidTagProviderUid

  
  
**S’applique à**: Outlook 
  
Contient une structure **MAPIUID** du fournisseur de services qui gère un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_UID  <br/> |
|Identificateur :  <br/> |0x300C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MAPI courantes  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

