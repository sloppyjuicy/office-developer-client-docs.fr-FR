---
title: Propriété canonique PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387201"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Propriété canonique PidTagSearchFolderTemplateId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ID du modèle qui est utilisé pour la recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Identificateur :  <br/> |0x6841  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Critères du dossier de recherche est spécifiée par un modèle. Cette propriété sur le message qui définit le dossier de recherche identifie le modèle correspondant. Outre la définition des critères de recherche, un modèle également définit les dossiers à exclure de la recherche, définit des éléments à exclure de la recherche et spécifie la valeur de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Pour plus d’informations sur les modèles de dossier de recherche, voir [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
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

