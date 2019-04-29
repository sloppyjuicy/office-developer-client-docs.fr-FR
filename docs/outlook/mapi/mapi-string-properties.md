---
title: Propriétés de chaîne MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431392"
---
# <a name="mapi-string-properties"></a>Propriétés de chaîne MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit trois types de propriétés différents pour décrire les propriétés de chaîne:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Les propriétés de chaîne sont généralement définies comme PT_TSTRING. Le type de propriété PT_TSTRING est compilé de manière conditionnelle sur l'un des autres types de propriété de chaîne, selon que la macro UNICODE a été définie ou non. PT_STRING8 décrit les chaînes de caractères de 8 bits se terminant par null au format ANSI; PT_UNICODE décrit les chaînes de caractères codés sur deux octets qui se terminent par null. 
  
Un fournisseur de services ou client, ou le client et le fournisseur peuvent choisir de prendre en charge les chaînes de caractères Unicode. Elle n'est pas obligatoire. Un client qui prend en charge uniquement les chaînes PT_STRING8 peut fonctionner avec un fournisseur qui prend en charge Unicode, et inversement. Pour activer cette interopérabilité, les clients et les fournisseurs de services transmettent un indicateur, l'indicateur MAPI_UNICODE, pour indiquer qu'Unicode est pris en charge dans les méthodes qui impliquent l'échange de chaînes de caractères. 
  
Par exemple, supposons qu'un client prend en charge Unicode et qu'il doive récupérer le nom d'affichage d'un dossier. Toutes les propriétés PT_TSTRING du client sont compilées en type PT_UNICODE. Lorsque le client appelle la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du dossier pour récupérer sa propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), il passe l'indicateur MAPI_UNICODE pour demander que la chaîne de nom d'affichage soit renvoyée au format Unicode. . 
  
Les clients et fournisseurs de services doivent savoir que la spécification d'un jeu de caractères dans un appel de méthode n'est qu'une requête. La prise en charge d'un ou des deux jeux de caractères est jusqu'à l'implémentation de l'objet. Toutefois, les fournisseurs de services sont encouragés à prendre en charge les deux jeux de caractères, car cela leur permet d'obtenir une distribution plus répandue que les fournisseurs qui ne prennent en charge qu'un seul ensemble. 
  
Les propriétés de chaîne peuvent devenir assez volumineuses en ce qui concerne les propriétés binaires, qui utilisent le type de propriété PT_BINARY. Pour faciliter l'utilisation des propriétés volumineuses, MAPI permet aux fournisseurs de services de définir ces propriétés afin d'appliquer des limites de taille. Ces limites peuvent varier en fonction des éléments suivants:
  
- Indique si les propriétés sont en cours de lecture ou d'écriture.
    
- Comment le fournisseur de services implémente les méthodes **IMAPIProp** . 
    
- Considérations relatives à l'exécution, telles que les contraintes de mémoire.
    
- Problèmes de conversion des jeux de caractères. 
    
Les limites de taille peuvent également être placées sur les propriétés de chaîne et binaires lorsqu'elles sont utilisées dans le jeu de colonnes d'un tableau car il est parfois impossible de rendre entièrement visible la valeur de la propriété large. De nombreux fournisseurs de services tronquent les grandes propriétés de chaîne ou binaires qui sont utilisées dans les tableaux à 255 octets. 
  
Lorsqu'un client appelle la méthode **GetProps** ou **SetProps** d'un objet pour fonctionner avec une chaîne ou une propriété binaire de grande taille et si l'appel échoue en raison de la taille de la propriété, la méthode renvoie la valeur d'erreur MAPI_E_NOT_ENOUGH_MEMORY. S'il s'agit d' **GetProps** qui échoue pour une propriété spécifique, le client peut effectuer une récupération en appelant [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et en demandant à l'accès **IStream** en spécifiant IID_IStream comme identificateur d'interface. À l'aide de **OpenProperty**, le client peut récupérer une grande propriété à l'aide d'une interface telle que **IStream** , mieux adaptée à l'utilisation de propriétés volumineuses. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

