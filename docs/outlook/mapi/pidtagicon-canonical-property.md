---
title: PidTagIcon Canonical, propriété
description: Décrit la propriété canonique PidTagIcon, qui contient une image bitmap d’une icône de taille complète pour un formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
ms.openlocfilehash: cc3b0b05147e5d14d279ae369f9c8243e9216f69
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770690"
---
# <a name="pidtagicon-canonical-property"></a>PidTagIcon Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une image bitmap d’une icône de taille complète pour un formulaire. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ICON  <br/> |
|Identificateur :  <br/> |0x0FFD  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image de 32 × 32 pixels d’une icône, identique au contenu d’une icône. Fichier ICO. Cette propriété est normalement copiée à partir du . Fichier ICO spécifié dans la ligne LargeIcon de la section [Description] appropriée du fichier de configuration de formulaire. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[PidTagMiniIcon Canonical, propriété](pidtagminiicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

