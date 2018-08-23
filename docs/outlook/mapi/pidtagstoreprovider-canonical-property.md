---
title: Propriété canonique PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595355"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Propriété canonique PidTagStoreProvider

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une structure [MAPIUID](mapiuid.md) défini par le fournisseur qui indique le type de la banque de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MDB_PROVIDER  <br/> |
|Identificateur :  <br/> |0x3414  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

La structure [MAPIUID](mapiuid.md) identifie le type de banque de messages. La valeur est calculée par les fournisseurs de banque de messages sur des objets de banque de messages et est unique pour chaque fournisseur. Il est généralement utilisé pour la navigation par le biais de la table de banque de messages pour rechercher un magasin du type souhaité, tels que les dossiers publics. 
  
Cette propriété correspond à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d’adresses. 
  
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

