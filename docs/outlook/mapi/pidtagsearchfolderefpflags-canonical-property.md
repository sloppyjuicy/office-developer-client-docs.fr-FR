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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e98416ba7796c66d719adcc27ba8029b7908bb79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786758"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a>Propriété canonique PidTagSearchFolderEfpFlags

  
  
**S’applique à**: Outlook 
  
Contient des indicateurs de dossier étendu qui s’appliquent à un conteneur de dossier de recherche pour le dossier de recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_EFP_FLAGS  <br/> |
|Identificateur :  <br/> |0x6848  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Search  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit contenir spécifiquement les indicateurs de la propriété **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) et la sous-propriété **ExtendedFlags** , dans le champ b pour le dossier. Pour plus d’informations sur les indicateurs de dossier, consultez [[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.
    
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

