---
title: Section [Extensions] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573557"
---
# <a name="form-configuration-file-extensions-section"></a>Section [Extensions] du fichier de configuration de formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La section **[Extensions]** répertorie les attributs étendus du formulaire, généralement un ensemble de la propriété nommée, qui sont des attributs au-delà de base celles répertoriées dans la section **[Description]** du fichier de configuration du formulaire. Les attributs étendus sont les propriétés retournées par les appels à la méthode **GetProps** de l’objet **IMAPIFormInfo** avec le bit élevé défini dans la balise de propriété. Les applications clientes peuvent déterminer les attributs étendus d’un formulaire, le cas échéant, en récupérant ces balises. Pour ce faire, les clients appelez la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , en passant les noms des propriétés du formulaire et appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir les propriétés. 
  
 **[Extensions]**
  
 **Extension.** _la chaîne string1_ =  _chaîne2_
  
Chaque section de la propriété extension définit un attribut d’extension à l’aide de l’interface MAPI nommée la syntaxe de la propriété. Le type de propriété doit être PT_LONG ou PT_STRING8. Jeux de propriétés qui contient les chaînes nommées ne sont pas pris en charge. Le format de la section **[Extension]** est la suivante : 
  
 **[Extension.** _chaîne2_ **]**
  
 **Type de** =  _entier_
  
 **NmidPropset** =  _guid_
  
 **Touche** =  _entier_
  
 **Valeur** =  _chaîne_ |  _entier_
  
Voici un exemple d’une section **[Extensions]** et une autre section connexe suivant. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


