---
title: Propriétés canoniques MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540475"
---
# <a name="mapi-canonical-properties"></a>Propriétés canoniques MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une propriété canonique est une propriété virtuelle qui représente une propriété MAPI ou plusieurs propriétés MAPI définies avec le même identificateur de propriété. Les propriétés canoniques sont conçues uniquement pour faciliter l’identification cohérente des propriétés MAPI dans les discussions ou la documentation en dehors du code. Contrairement aux noms de propriétés balisés définis par MAPI, les noms des propriétés canoniques ne sont pas définis en tant que constantes globales dans les fichiers d’en-tête MAPI.
  
## <a name="naming-conventions"></a>Conventions d’attribution de noms

Les noms des propriétés canoniques commencent par un préfixe, « Pid », qui représente « identificateur de propriété ». Selon que la propriété est une propriété marquée, une propriété nommée avec un identificateur numérique ou une propriété nommée avec un nom de chaîne, le préfixe est qualifié en tant que « PidTag », « PidLid » et « PidName », respectivement. Par exemple, [PidTagAccount](pidtagaccount-canonical-property.md) représente les propriétés marquées, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) et **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), qui spécifient le nom de compte d’un destinataire ; [PidLidContacts](pidlidcontacts-canonical-property.md) représente la propriété **dispidContacts,** une propriété nommée qui possède un identificateur numérique et qui spécifie le nom des contacts associés à un message ; et [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) représente « , » une propriété nommée qui a un nom de chaîne et qui spécifie les messages de marquage de chaîne susceptibles d’être du http://schemas.microsoft.com/outlook/phishingstamp hameçonnage. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Représentation de propriétés similaires à l’aide d’une propriété canonique

### <a name="identifying-properties-in-mapi"></a>Identification des propriétés dans MAPI

Toutes les propriétés dans MAPI sont identifiées par un identificateur de propriété qui est une valeur 16 bits non signée. L’identificateur de propriété et le type de propriété (une autre valeur 16 bits non signée) constituent une balise de propriété pour la propriété. 
  
MAPI utilise une balise de propriété pour définir des propriétés de manière unique. Les propriétés qui ont la même balise de propriété, comme **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) et **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), sont considérées comme des propriétés identiques dans MAPI. Pour obtenir la liste des balises de propriété que MAPI a définies pour ses propres propriétés, voir le fichier d’en-tête MAPI Mapitags.h.
  
Notez que MAPI divise les identificateurs de propriété en plages. L’endroit où un identificateur se trouve dans la plage indique son utilisation et sa propriété. Les identificateurs de propriétés des propriétés marquées sont 0x0001 à 0x7FFF. Dans cette plage se trouve les identificateurs de propriétés des propriétés définies par MAPI, qui sont dans la plage de 0x0001 à 0x3FFF. Les identificateurs de propriété des propriétés nommées sont dans la plage de 0x8000 à 0x8FFF. 
  
Les propriétés nommées sont en outre attribuées par un jeu de propriétés, ainsi qu’un ID long (LID), qui est une valeur 32 bits non signée, ou une chaîne. Un jeu de propriétés est un GUID qui identifie un groupe de propriétés nommées ayant un objectif similaire. Le jeu de propriétés et le nom DE LAT ou de chaîne sont utilisés pour obtenir ou définir la propriété nommée.
  
### <a name="property-type"></a>Type de propriété

Outre les identificateurs, une propriété est attribuée par un type de données qui spécifie le type de valeurs autorisées pour cette propriété.
  
Pour les propriétés de type chaîne, selon la prise en charge d’Unicode dans la plateforme sous-jacente, la propriété peut être de type PT_STRING8 (chaîne de caractères 8 bits terminée par null) ou PT_UNICODE (chaîne Unicode terminée par null). Une propriété peut être définie avec le type PT_TSTRING et, selon les paramètres de compilation, PT_TSTRING est définie par défaut sur une chaîne Unicode pour les plateformes qui prendre en charge Unicode ou sur une chaîne PT_STRING8 pour les plateformes qui prendre en charge ANSI ou DBCS. Il est courant qu’une propriété de type chaîne soit identifiée par trois noms similaires, tels que **PR_ACCOUNT,** **PR_ACCOUNT_A** et **PR_ACCOUNT_W,** qui sont de type PT_TSTRING, PT_STRING8 et PT_UNICODE respectivement.
  
Pour plus d’informations sur les types de propriétés et les macros liés aux types, voir le fichier d’en-tête MAPI Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identification de propriétés similaires

Dans le paysage actuel des propriétés MAPI, il n’est pas rare qu’une propriété ait été exposée sous différents noms de propriétés, qui sont tous définis avec le même identificateur de propriété. Par exemple, les propriétés marquées, **PR_BUSINESS2_TELEPHONE_NUMBER** et **PR_OFFICE2_TELEPHONE_NUMBER**, sont définies dans Mapitags.h pour avoir le même identificateur et le même type de propriété. Étroitement liées à ces deux propriétés sont :
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Les propriétés avec le suffixe « _A » sont typés en tant que PT_STRING8, et celles avec le suffixe « _W » sont typés comme PT_UNICODE.
  
L’objectif d’une propriété canonique, **PidTagBusiness2TelephoneNumber** dans cet exemple, est de faciliter le référencement de ces propriétés MAPI étroitement affiliés à l’aide d’un identificateur et de manière cohérente (à l’aide du préfixe « Pid » ) sur toutes les propriétés MAPI. Pour connaître les propriétés MAPI réelles représentées par une propriété canonique, voir [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md). Pour trouver la propriété canonique à qui une propriété MAPI est associée, voir Mappage des noms MAPI aux noms [de propriétés canoniques.](mapping-mapi-names-to-canonical-property-names.md)
  
## <a name="mapi-support-of-canonical-property-names"></a>Prise en charge MAPI des noms de propriétés canoniques

Étant donné que les propriétés canoniques ne sont pas des propriétés réelles et ne sont pas définies dans les fichiers d’en-tête MAPI, vous ne devez pas utiliser de noms de propriétés canoniques dans le code ; à la place, vous devez continuer à utiliser les noms de propriété MAPI exacts dans le code. Par exemple, vous pouvez faire référence **PR_BUSINESS2_TELEPHONE_NUMBER** et **PR_OFFICE2_TELEPHONE_NUMBER** en dehors du code en tant que  **PidTagBusiness2TelephoneNumber** et utiliser PR_BUSINESS2_TELEPHONE_NUMBER ou **PR_OFFICE2_TELEPHONE_NUMBER** dans le code. 
  
Si vous devez utiliser des noms de propriétés canoniques dans votre code, vous devez d’abord les définir dans vos propres fichiers d’en-tête.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Noms des propriétés canoniques et spécifications du protocole Exchange

Les noms canoniques sont référencés dans Microsoft Exchange Server spécifications de protocole utilisées par les Exchange Server pour communiquer avec d’autres produits Microsoft. Pour plus d’informations sur les propriétés d’objet de message référencés par les spécifications du protocole Exchange, voir [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[Balises de propriété MAPI](mapi-property-tags.md)
  
[Vue d’ensemble de l’identificateur de propriété MAPI](mapi-property-identifier-overview.md)
  
[Vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md)

