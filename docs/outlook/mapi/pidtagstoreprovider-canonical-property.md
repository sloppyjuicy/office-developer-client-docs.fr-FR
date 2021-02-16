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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412050"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Propriété canonique PidTagStoreProvider

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une structure [MAPIUID](mapiuid.md) définie par un fournisseur qui indique le type de la magasin de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MDB_PROVIDER  <br/> |
|Identificateur :  <br/> |0x3414  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de l’ID  <br/> |
   
## <a name="remarks"></a>Remarques

La structure [MAPIUID](mapiuid.md) identifie le type de magasin de messages. La valeur est calculée par les fournisseurs de magasins de messages sur les objets de la boutique de messages et est propre à chaque fournisseur. Il est généralement utilisé pour parcourir la table de la boutique de messages afin de trouver une boutique du type souhaité, par exemple des dossiers publics. 
  
Cette propriété est analogue à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d’adresses. 
  
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

