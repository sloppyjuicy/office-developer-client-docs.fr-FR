---
title: Propriété canonique PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385944"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a>Propriété canonique PidTagSearchFolderExpiration

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’heure à laquelle le conteneur de dossiers de recherche sera obsolète et doit être mis à jour ou recréé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_EXPIRATION  <br/> |
|Identificateur :  <br/> |0x683A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être mis en forme en tant que le nombre de minutes depuis minuit temps universel coordonné (UTC) le 1er janvier 1601.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
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

