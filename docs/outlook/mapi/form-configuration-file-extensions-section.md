---
title: Section de formulaire Configuration de fichier [Extensions]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783326"
---
# <a name="form-configuration-file-extensions-section"></a>Section de formulaire Configuration de fichier [Extensions]

  
  
**S’applique à**: Outlook 
  
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


