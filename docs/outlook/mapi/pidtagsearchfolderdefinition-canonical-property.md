---
title: Propriété canonique PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2f17f273afc3f2537195cde21c7bc30626b13a26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573201"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Propriété canonique PidTagSearchFolderDefinition

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des données qui spécifie les critères de recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Identificateur :  <br/> |0x6845  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Le contenu spécifique de chaque champ de l’objet binaire volumineux (BLOB) contenue dans cette propriété dépend de l’ID du modèle spécifié dans la propriété **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)). Pour plus d’informations sur les modèles de structure et la recherche des objets BLOB, voir [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
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

