---
title: Propriété canonique PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 30569efe44960486940e0b39b44ca43d911a8b76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561039"
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

