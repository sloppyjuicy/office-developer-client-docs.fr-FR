---
title: Propriété canonique PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336427"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a>Propriété canonique PidTagSearchFolderEfpFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des indicateurs de dossier étendu qui s’appliquent au conteneur de dossiers de recherche pour le dossier de recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_EFP_FLAGS  <br/> |
|Identificateur :  <br/> |0x6848  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit contenir spécifiquement les indicateurs dans la propriété **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) et la sous-propriété **ExtendedFlags,** dans le champ b du dossier. Pour plus d’informations sur les indicateurs de dossier, [voir [MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de manipulation d’une configuration de liste de dossiers de recherche.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.
    
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

