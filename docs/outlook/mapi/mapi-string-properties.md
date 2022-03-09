---
title: Propriétés de chaîne MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
ms.openlocfilehash: c14b49746b78b5cbb47f6eea9008b99f8728a00a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377763"
---
# <a name="mapi-string-properties"></a>Propriétés de chaîne MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit trois types de propriétés différents pour décrire les propriétés de chaîne :
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Les propriétés de chaîne sont généralement définies comme PT_TSTRING. Le PT_TSTRING type de propriété est compilé de manière conditionnable dans l’un des autres types de propriétés de chaîne, selon que la macro UNICODE a été définie ou non. PT_STRING8 décrit les chaînes de caractères terminées par null sur 8 bits au format ANSI ; PT_UNICODE décrit les chaînes de caractères terminées par des caractères sur deux caractères. 
  
Un client ou un fournisseur de services, ou les deux clients et fournisseurs peuvent choisir de prendre en charge les chaînes de caractères Unicode. Elle n’est pas obligatoire. Un client qui prend en charge uniquement PT_STRING8 chaînes peuvent fonctionner avec un fournisseur qui prend en charge Unicode et vice versa. Pour activer cette interopérabilité, les clients et les fournisseurs de services passent un indicateur, l’indicateur MAPI_UNICODE, pour indiquer que Unicode est pris en charge dans les méthodes qui impliquent l’échange de chaînes de caractères. 
  
Par exemple, supposons qu’un client prend en charge Unicode et doit récupérer le nom complet d’un dossier. Toutes les propriétés de PT_TSTRING client sont compilées pour taper PT_UNICODE. Lorsque le client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du dossier pour récupérer sa propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), il transmet l’indicateur MAPI_UNICODE pour demander que la chaîne de nom complet soit renvoyée au format Unicode. 
  
Les clients et les fournisseurs de services doivent savoir que spécifier un jeu de caractères dans un appel de méthode n’est qu’une demande. L’implémenteur de l’objet doit prendre en charge un ou les deux jeux de caractères. Toutefois, les fournisseurs de services sont encouragés à prendre en charge les deux jeux de caractères, car il leur permet d’obtenir une distribution plus étendue que les fournisseurs qui ne le supportent qu’un seul. 
  
Les propriétés de chaîne peuvent devenir assez grandes, tout comme les propriétés binaires qui utilisent le type de propriété PT_BINARY. Pour faciliter l’travail avec des propriétés de grande taille, MAPI permet aux fournisseurs de services de définir ces propriétés pour appliquer des limites de taille. Ces limites peuvent varier en fonction des éléments suivants :
  
- Si les propriétés sont en cours de lecture ou d’écriture.
    
- La façon dont le fournisseur de services implémente **les méthodes IMAPIProp** . 
    
- Considérations d’runtime, telles que les contraintes de mémoire.
    
- Problèmes de traduction de jeu de caractères. 
    
Les limites de taille peuvent également être placées sur des propriétés de chaîne et binaires lorsqu’elles sont utilisées dans le jeu de colonnes d’un tableau, car il est parfois impossible de rendre visible l’ensemble de la valeur d’une propriété de grande taille. De nombreux fournisseurs de services tronquéent les propriétés binaires ou de chaîne de grande taille utilisées dans les tableaux à 255 octets. 
  
Lorsqu’un client appelle la méthode **GetProps** ou **SetProps** d’un objet pour fonctionner avec une grande chaîne ou une propriété binaire et que l’appel échoue en raison de la taille de la propriété, la méthode renvoie la valeur d’erreur MAPI_E_NOT_ENOUGH_MEMORY. Si **getProps** échoue pour une propriété spécifique, le client peut récupérer en appelant [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et en demandant l’IStream pour  l’accès en spécifiant IID_IStream comme identificateur d’interface. À **l’aide d’OpenProperty**, le client peut récupérer une propriété de grande taille à l’aide d’une interface telle que **IStream** qui convient mieux à l’utilisation de propriétés de grande taille. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

