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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422774"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propriété canonique PidTagProviderUid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une structure **MAPIUID** du fournisseur de services qui gère un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_UID  <br/> |
|Identificateur :  <br/> |0x300C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par tous les fournisseurs de services. Il contient une structure [MAPIUID](mapiuid.md) associée au fournisseur et généralement codée en dur. Il est généralement utilisé par une application cliente qui s’intéresse uniquement aux conteneurs de carnet d’adresses fournis par un fournisseur particulier. 
  
Cette propriété apparaît uniquement en tant qu’entrée de colonne dans la table fournisseur.
  
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

