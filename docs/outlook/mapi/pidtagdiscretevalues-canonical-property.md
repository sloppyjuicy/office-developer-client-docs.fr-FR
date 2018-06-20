---
title: Propriété canonique PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785954"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propriété canonique PidTagDiscreteValues

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un rapport de non-remise s’applique uniquement à des membres d’une liste de distribution plutôt que l’intégralité de la liste. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificateur :  <br/> |0x0E0E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans un rapport de non-remise lorsque le message n’a pas pu être remis à un ou plusieurs membres d’une liste de distribution. Son objectif est de limiter retransmission tente seuls les membres individuels et pas la liste de distribution dans sa globalité. 
  
La table de destinataires d’un rapport de non-remise contient les entrées de tous les destinataires auxquels le message pas pu être remis, ainsi que pour les listes de distribution, le cas échéant, auxquels ils appartiennent. Le fournisseur de transport doit définir cette propriété sur TRUE pour chaque entrée de liste de distribution, et il doit copier les **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **clé PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) à partir de la liste de distribution **PR_ORIGINAL_SEARCH_KEY** ([ , **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) et **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)) PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) Propriétés pour chaque membre de cette liste de distribution. 
  
 **PR_DISCRETE_VALUES** ne doit pas être défini pour une entrée de destinataire de rapport de non-remise autre qu’une liste de distribution. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

