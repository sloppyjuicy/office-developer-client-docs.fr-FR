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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786466"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriété canonique PidTagProviderOrdinal

  
  
**S’applique à**: Outlook 
  
Contient l’index de base zéro de la position d’un fournisseur de service dans la table fournisseur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificateur :  <br/> |0x300D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |MAPI courantes  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

