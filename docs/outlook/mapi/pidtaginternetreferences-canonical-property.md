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
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360409"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propriété canonique PidTagInternetReferences

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du champ d'en-tête références d'un message MIME (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificateur :  <br/> |0x1039  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d'en-tête References, les clients doivent définir ces propriétés sur la valeur souhaitée. Les enregistreurs MIME doivent copier la valeur de ces propriétés dans le champ d'en-tête References.
  
Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée dans un champ d'en-tête References. Les lecteurs MIME doivent copier la valeur du champ d'en-tête références sur ces propriétés. Les lecteurs MIME peuvent tronquer la valeur de ces propriétés si elles dépassent la longueur de 64 Ko.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

