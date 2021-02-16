---
title: Propriété canonique PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422242"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propriété canonique PidTagAbProviderId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la structure [MAPIUID](mapiuid.md) d’un fournisseur de carnet d’adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificateur :  <br/> |0x3615  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

La structure **MAPIUID** identifie le fournisseur de carnet d’adresses qui fournit ce conteneur particulier dans la hiérarchie de conteneurs. La valeur est propre à chaque fournisseur. 
  
Un fournisseur de carnet d’adresses peut fournir plusieurs identificateurs. Par exemple, un fournisseur qui fournit  deux conteneurs différents peut publier dans PR_AB_PROVIDER_ID identificateurs uniques pour chaque conteneur. 
  
 **PR_AB_PROVIDER_ID** est analogue à la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour les magasins de messages. Les applications clientes peuvent **utiliser PR_AB_PROVIDER_ID** pour rechercher des lignes associées dans une table de hiérarchie de carnet d’adresses. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[Propriété canonique PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

