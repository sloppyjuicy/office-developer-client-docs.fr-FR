---
title: Propriété canonique PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573809"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriété canonique PidTagProviderOrdinal

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’index de base zéro de la position d’un fournisseur de service dans la table fournisseur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificateur :  <br/> |0x300D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI.
  
Obtenir la table fournisseur en appelant la méthode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) . Trier le tableau de fournisseur de cette propriété pour afficher l’ordre de transport. 
  
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

