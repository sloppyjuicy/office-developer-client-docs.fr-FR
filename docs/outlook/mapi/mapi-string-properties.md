---
title: Propriétés de type chaîne MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572325"
---
# <a name="mapi-string-properties"></a>Propriétés de type chaîne MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI propose trois différents types de propriété pour décrire les propriétés de type chaîne :
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Propriétés de type chaîne sont généralement définies comme PT_TSTRING. Le type de propriété PT_TSTRING compilation conditionnelle à un des autres types de propriété de chaîne, selon selon si la macro UNICODE a été définie. PT_STRING8 décrit des chaînes de caractères terminée par le caractère null de 8 bits au format ANSI ; PT_UNICODE décrit les chaînes de caractères terminée par le caractère null. 
  
Soit un client ou un fournisseur de services, ou à la fois client et fournisseur la possibilité de prendre en charge des chaînes de caractères Unicode. Il n’est pas obligatoire. Un client qui prend en charge uniquement les chaînes PT_STRING8 peut fonctionner avec un fournisseur qui prend en charge Unicode et vice versa. Pour activer cette interopérabilité, clients et fournisseurs de services de transmettent un indicateur, l’indicateur MAPI_UNICODE, pour indiquer que Unicode est pris en charge dans les méthodes qui impliquent l’échange des chaînes de caractères. 
  
Par exemple, supposons qu’un client prend en charge Unicode et a besoin de récupérer le nom complet d’un dossier. Toutes les propriétés PT_TSTRING du client sont compilés en type PT_UNICODE. Lorsque le client appelle la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) du dossier à récupérer sa propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), il passe l’indicateur MAPI_UNICODE pour demander que renvoyer la chaîne du nom complet dans le format Unicode . 
  
Fournisseurs de services et les clients doivent connaître spécifiant un jeu de caractères dans un appel de méthode est uniquement une demande. Prise en charge d’un ou deux jeux de caractères dépend de l’implémentation de l’objet. Toutefois, les fournisseurs de services sont invités à prendre en charge les deux jeux de caractères, car il leur permet d’atteindre la distribution plus large que les fournisseurs qui prennent en charge qu’un seul ensemble. 
  
Propriétés de type chaîne peuvent devenir très volumineux comme propriétés binaires, les propriétés qui utilisent la propriété type PT_BINARY. Pour faciliter l’utilisation des propriétés de grande taille, MAPI permet de fournisseurs de services de définition de ces propriétés appliquer des limites de taille. Ces limites peuvent varier, en fonction de :
  
- Indique si les propriétés sont en cours lu ou écrit.
    
- Comment le fournisseur de services implémente les méthodes **IMAPIProp** . 
    
- Considérations de runtime, telles que des contraintes de mémoire.
    
- Problèmes de traduction du jeu de caractères. 
    
Limites de taille peuvent également être placés sur une chaîne et propriétés binaires lorsqu’ils sont utilisés dans la colonne valeur d’une table car il est parfois impossible afficher tous les valeur d’une propriété de grande taille. Plusieurs fournisseurs de services tronquent la chaîne de grande taille ou des propriétés binaires qui sont utilisées dans les tableaux à 255 octets. 
  
Lorsqu’un client appelle la méthode **GetProps** ou **SetProps** d’un objet pour travailler avec une chaîne de grande taille ou une propriété binaire et l’appel échoue en raison de la taille de la propriété, la méthode renvoie la valeur d’erreur MAPI_E_NOT_ENOUGH_MEMORY. S’il est **GetProps** qui ont échoué pour une propriété spécifique, le client peut récupérer en appelant [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et en demandant **IStream** pour l’accès en spécifiant l’identificateur d’interface IID_IStream. À l’aide de **OpenProperty**, le client peut extraire une propriété de grande taille à l’aide d’une interface comme **IStream** qui convient mieux pour l’utilisation des propriétés de grande taille. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

