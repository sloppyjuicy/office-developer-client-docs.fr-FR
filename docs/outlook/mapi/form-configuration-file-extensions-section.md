---
title: Section Fichier de configuration de formulaire [Extensions]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
ms.openlocfilehash: 07f079328b3d577063f24c83198c29dba8a92586
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370679"
---
# <a name="form-configuration-file-extensions-section"></a>Section Fichier de configuration de formulaire [Extensions]

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Extensions]** répertorie les attributs étendus du formulaire, généralement un jeu de propriétés nommé, qui sont des attributs autres que les attributs de base répertoriés dans la section **[Description]** du fichier de configuration du formulaire. Les attributs étendus sont des propriétés renvoyées par les appels à la méthode **GetProps** de l’objet **IMAPIFormInfo** avec le bit élevé de la balise de propriété. Les applications clientes peuvent déterminer les attributs étendus d’un formulaire, s’il y en a, en récupérant ces balises. Pour ce faire, les clients appellent la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , en passant les noms des propriétés du formulaire et en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir les propriétés. 
  
 **[Extensions]**
  
 **Extension.** _string1_ =   _string2_
  
Chaque section de propriété d’extension définit un attribut d’extension à l’aide de la syntaxe de propriété nommée MAPI. Le type de propriété doit être PT_LONG ou PT_STRING8. Les jeux de propriétés qui contiennent des chaînes nommées ne sont pas pris en charge. Le format de la section **[Extension]** est le suivante : 
  
 **[Extension.** _string2_ **]**
  
 **Type** =   _integer_
  
 **NmidPropset** =   _guid_
  
 **NmidInteger** =   _integer_
  
 **Valeur** =   _string_ |   _integer_
  
Voici un exemple de section **[Extensions]** et une section connexe suivante. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


