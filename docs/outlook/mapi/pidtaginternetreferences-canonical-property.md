---
title: Propriété canonique PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786131"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propriété canonique PidTagInternetReferences

  
  
**S’applique à**: Outlook 
  
Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) références.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificateur :  <br/> |0x1039  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d’en-tête références, les clients doivent définir ces propriétés à la valeur souhaitée. Rédacteurs MIME doivent copier la valeur de ces propriétés sur le champ d’en-tête de références.
  
Pour définir la valeur de ces propriétés, clients MIME doivent écrire la valeur souhaitée dans un champ d’en-tête de références. Lecteurs MIME doivent copier la valeur du champ d’en-tête références sur ces propriétés. Lecteurs MIME peuvent tronquer la valeur de ces propriétés s’il dépasse 64 Ko de longueur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
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

