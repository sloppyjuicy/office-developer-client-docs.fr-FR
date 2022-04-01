---
title: Propriété canonique PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: Contient des données qui spécifient les critères de recherche pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 8963cd8022938d8ecde513f4e5a94e0bf33e7eac
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524235"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Propriété canonique PidTagSearchFolderDefinition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des données qui spécifient les critères de recherche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Identificateur :  <br/> |0x6845  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Rechercher  <br/> |
   
## <a name="remarks"></a>Remarques

Le contenu spécifique de chaque champ de l’objet BLOB (Binary Large Object) contenu dans cette propriété dépend de l’ID de modèle spécifié dans la propriété **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)). Pour plus d’informations sur la structure BLOB et les modèles de recherche, voir [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de manipulation d’une configuration de liste de dossiers de recherche.
    
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

