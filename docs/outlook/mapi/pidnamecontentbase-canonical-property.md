---
title: Propriété canonique PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: Contient une valeur de champ d’en-tête content-base RFC3282. Pour définir la valeur, les clients MIME doivent écrire la valeur dans un champ d’en-tête Content-Base sur une entité MIME dans le corps du message.
ms.openlocfilehash: 9ce2ea711293c62374200516c42dc17d6f682a51
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764684"
---
# <a name="pidnamecontentbase-canonical-property"></a>Propriété canonique PidNameContentBase

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de champ d’en-tête Content-Base [RFC3282].
  
|Propriété |Valeur |
|:-----|:-----|
|Noms convivial :  <br/> |BodyContentBase  <br/> |
|Jeu de propriétés :  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété :  <br/> |Content-Base  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message Extensions) doivent écrire la valeur souhaitée dans un champ d’en-tête Content-Base sur une entité MIME migré à un corps de message. Les lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Base sur une entité MIME de ce type vers la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

