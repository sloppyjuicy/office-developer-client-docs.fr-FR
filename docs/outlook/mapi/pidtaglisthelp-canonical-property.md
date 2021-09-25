---
title: Propriété canonique PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1a67eaac19fb6316825f890207e061d958be791f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613358"
---
# <a name="pidtaglisthelp-canonical-property"></a>Propriété canonique PidTagListHelp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du champ d’en-tête MIME (Multipurpose Internet Mail Extensions) List-Help'en-tête.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Identificateur :  <br/> |0x1043  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un List-Help d’en-tête, les  clients doivent définir la valeur de PR_LIST_HELP ou une propriété associée sur la valeur souhaitée. Les rédacteurs MIME doivent copier cette valeur dans le champ List-Help'en-tête. 
  
Pour définir la valeur de ces propriétés liées au serveur de liste, les clients MIME doivent écrire les champs d’en-tête comme indiqué dans le tableau suivant :
  
|**Propriété**|**Nom de champ d’en-tête préféré**|**Autre nom de champ d’en-tête**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |List-Help  <br/> |X-List-Help  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
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

