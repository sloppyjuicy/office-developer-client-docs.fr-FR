---
title: Propriété canonique PidTagInternetReferences
description: Décrit la propriété canonique PidTagInternetReferences, qui contient la valeur du champ d’en-tête Références d’un message MIME.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
ms.openlocfilehash: f9a6bef36a45d440cdedbb5fe7be87db42c77456
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752651"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propriété canonique PidTagInternetReferences

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du champ d’en-tête Références d’un message MIME (Multipurpose Internet Mail Extensions).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificateur :  <br/> |0x1039  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d’en-tête Références, les clients doivent définir ces propriétés sur la valeur souhaitée. Les enregistreurs MIME doivent copier la valeur de ces propriétés dans le champ d’en-tête Références.
  
Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée dans un champ d’en-tête Références. Les lecteurs MIME doivent copier la valeur du champ d’en-tête Références dans ces propriétés. Les lecteurs MIME peuvent tronquer la valeur de ces propriétés s’ils dépassent 64 Ko de longueur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

