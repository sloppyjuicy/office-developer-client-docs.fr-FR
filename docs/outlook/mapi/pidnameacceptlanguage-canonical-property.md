---
title: PidNameAcceptLanguage, propriété canonique
description: Décrit la propriété canonique PidNameAcceptLanguage, qui contient une valeur de champ d’en-tête [RFC3282] Accept-Language.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
ms.openlocfilehash: 655e34de3db1e02d71eb3bc438882462adc0e0c7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817367"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>PidNameAcceptLanguage, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de champ d’en-tête [RFC3282] Accept-Language.
  
|Propriété|Valeur|
|:-----|:-----|
|Noms conviviaux :  <br/> |AcceptLanguage  <br/> |
|Jeu de propriétés :  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété :  <br/> |Accept-Language  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message Extensions) doivent écrire un champ d’en-tête Accept-Language avec la valeur souhaitée. Les clients MIME peuvent écrire un champ d’en-tête X-Accept-Language à la place. Les lecteurs MIME doivent copier la valeur de l’un ou l’autre champ d’en-tête vers la valeur de cette propriété. Si les deux champs d’en-tête sont présents, les lecteurs MIME doivent utiliser le champ d’en-tête Accept-Language.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

