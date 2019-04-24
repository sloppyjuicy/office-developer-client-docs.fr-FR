---
title: Propriété canonique PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279628"
---
# <a name="pidtaglisthelp-canonical-property"></a>Propriété canonique PidTagListHelp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur d'un champ d'en-tête d'aide sur la liste des messages MIME (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Identificateur :  <br/> |0x1043  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d'en-tête d'aide sur la liste, les clients doivent définir la valeur de **PR_LIST_HELP** ou une propriété associée sur la valeur souhaitée. Les enregistreurs MIME doivent copier cette valeur dans le champ d'en-tête de liste d'aide. 
  
Pour définir la valeur de ces propriétés liées au serveur de liste, les clients MIME doivent écrire les champs d'en-tête comme indiqué dans le tableau suivant:
  
|**Property**|**Nom de champ d'en-tête préféré**|**Nom de champ d'en-tête secondaire**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |Liste-aide  <br/> |X-List-aide  <br/> |
   
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

