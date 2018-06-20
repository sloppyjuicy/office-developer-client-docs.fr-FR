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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785647"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propriété canonique PidTagAbProviderId

  
  
**S’applique à**: Outlook 
  
Contient la structure [MAPIUID](mapiuid.md) d’un fournisseur de carnet d’adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificateur :  <br/> |0x3615  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

La structure **MAPIUID** identifie le fournisseur de carnet d’adresses fournit ce conteneur particulier dans la hiérarchie des conteneurs. La valeur est unique pour chaque fournisseur. 
  
Un fournisseur de carnet d’adresses peut fournir plusieurs identificateurs. Par exemple, un fournisseur qui fournit deux différents conteneurs peut publier dans **PR_AB_PROVIDER_ID** des identificateurs uniques pour chaque conteneur. 
  
 **PR_AB_PROVIDER_ID** correspond à la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour les banques de messages. Les applications de client peuvent utiliser **PR_AB_PROVIDER_ID** pour rechercher des lignes dans une table de hiérarchie adresse téléchargeable. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[Propriété canonique PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

