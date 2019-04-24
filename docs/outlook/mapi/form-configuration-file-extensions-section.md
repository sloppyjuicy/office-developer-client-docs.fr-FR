---
title: Section [extensions] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327299"
---
# <a name="form-configuration-file-extensions-section"></a>Section [extensions] du fichier de configuration de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[extensions]** répertorie les attributs étendus du formulaire, généralement un jeu de propriétés nommé, qui sont des attributs autres que ceux de base répertoriés dans la section **[Description]** du fichier de configuration de formulaire. Les attributs étendus sont des propriétés retournées à partir d'appels à la méthode **GetProps** de l'objet **IMAPIFormInfo** avec le bit supérieur défini dans la balise property. Les applications clientes peuvent déterminer les attributs étendus d'un formulaire, le cas échéant, en extrayant ces balises. Pour ce faire, les clients appellent la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , en transmettant les noms des propriétés du formulaire et appellent la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir les propriétés. 
  
 **Long**
  
 **Long.** _chaîne1_ =  _Chaîne2_
  
Chaque section de propriété extension définit un attribut extension à l'aide de la syntaxe de propriété nommée MAPI. Le type de propriété doit être PT_LONG ou PT_STRING8. Les jeux de propriétés qui contiennent des chaînes nommées ne sont pas pris en charge. Le format de la section **[extension]** est le suivant: 
  
 **Long.** _Chaîne2_ **]**
  
 **Type** =  _entier_
  
 **** =  _GUID_ NmidPropset
  
 **** =  _Entier_ NmidInteger
  
 **** =  __ Chaîne |  de valeur_entière_
  
Vous trouverez ci-dessous un exemple de section **[extensions]** et une section associée ultérieure. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


