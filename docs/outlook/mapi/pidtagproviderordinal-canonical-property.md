---
title: Propriété canonique PidTagProviderOrdinal
description: Décrit la propriété canonique PidTagProviderOrdinal, qui contient l’index de base zéro de la position d’un fournisseur de services dans la table du fournisseur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
ms.openlocfilehash: 18ff563c46c54b5d1a2068ae1006cce92c27e40a
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752455"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriété canonique PidTagProviderOrdinal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’index de base zéro de la position d’un fournisseur de services dans la table du fournisseur.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificateur :  <br/> |0x300D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI.
  
Obtenez la table du fournisseur en appelant la méthode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) . Triez la table du fournisseur sur cette propriété pour afficher l’ordre de transport. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

