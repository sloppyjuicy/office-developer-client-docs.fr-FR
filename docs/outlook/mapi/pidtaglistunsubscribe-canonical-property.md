---
title: PidTagListUnsubscribe, propriété canonique
description: Décrit la propriété canonique PidTagListUnsubscribe, qui contient la valeur du champ d’en-tête List-Unsubscribe d’un message MIME.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
ms.openlocfilehash: 5d5a3c8971c16df6ba41107a13749a9c9ba32cdf
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752301"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>PidTagListUnsubscribe, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du champ d’en-tête List-Unsubscribe d’un message MIME (Multipurpose Internet Mail Extensions).
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Identificateur :  <br/> |0x1045  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d’en-tête List-Unsubscribe, les clients doivent définir ces propriétés sur la valeur souhaitée. Les enregistreurs MIME doivent copier la valeur de ces propriétés dans le champ d’en-tête List-Unsubscribe.
  
Pour définir la valeur de ces propriétés liées au serveur de liste, les clients MIME doivent écrire les champs d’en-tête comme spécifié dans le tableau suivant.
  
|**Propriété**|**Nom du champ d’en-tête préféré**|**Autre nom de champ d’en-tête**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |List-Unsubscribe  <br/> |X-List-Unsubscribe  <br/> |
   
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

