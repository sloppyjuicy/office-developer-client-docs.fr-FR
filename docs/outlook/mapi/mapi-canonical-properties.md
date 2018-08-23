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
ms.openlocfilehash: 82c44f2292400c449ee0f82600c5b596728af7c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590434"
---
# <a name="mapi-canonical-properties"></a>Propriétés canoniques MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une propriété canonique est une propriété virtuelle qui représente une propriété MAPI ou plusieurs propriétés MAPI définies avec le même identificateur de propriété. Propriétés canoniques sont uniquement destinées à faciliter l’identification cohérente des propriétés MAPI dans la documentation en dehors du code ou discussions. Contrairement aux noms de propriété avec balise MAPI définie, les noms de propriété canonique ne sont pas définies comme des constantes globales dans les fichiers d’en-tête MAPI.
  
## <a name="naming-conventions"></a>Conventions d’affectation de noms

Les noms de propriété canonique commencent par un préfixe « Pid », qui représente l’identificateur de propriété «. » Selon que la propriété est une propriété balise, une propriété nommée avec un identificateur numérique ou une propriété nommée avec un nom de chaîne, le préfixe est également appelée « PidTag », « PidLid » et « PidName », respectivement. Par exemple, [PidTagAccount](pidtagaccount-canonical-property.md) représente les propriétés balisées, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) et **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), qui spécifient d’un destinataire nom du compte ; [PidLidContacts](pidlidcontacts-canonical-property.md) représente la propriété **dispidContacts** , une propriété nommée qui possède un identificateur numérique et qui spécifie le nom des contacts associés à un message ; et représente [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) »http://schemas.microsoft.com/outlook/phishingstamp, « une propriété nommée ayant un nom de chaîne, et qui spécifie la chaîne de marquage des messages qui sont susceptibles d’être hameçonnage. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Représentant les propriétés similaires à l’aide d’une propriété canonique

### <a name="identifying-properties-in-mapi"></a>Identification des propriétés MAPI

Toutes les propriétés MAPI sont identifiées par un identificateur de la propriété est une valeur de 16 bits non signée. Identificateur de la propriété et le type de propriété (une autre valeur de 16 bits non signé) constituent une balise de propriété pour la propriété. 
  
MAPI utilise une balise de propriété pour définir les propriétés de façon unique. Propriétés qui ont la même balise de propriété, tels que **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) et **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), sont considérés comme identiques propriétés MAPI. Pour obtenir la liste des balises de propriété MAPI a défini pour ses propres propriétés, voir le fichier d’en-tête MAPI Mapitags.h.
  
Notez que MAPI divise les identificateurs de propriété dans des plages. Où un identificateur fait partie de la plage indique son utilisation et propriété. Les identificateurs de propriété des propriétés avec balise peuvent être classées dans la plage 0 x 0001 à 0x7FFF. Dans cette plage sont les identificateurs de propriété des propriétés définies par MAPI, qui peuvent être classées dans la plage 0 x 0001 à 0x3FFF. Les identificateurs de propriété de diminution de propriétés nommées dans la plage 0 x 8000 à 0x8FFF. 
  
Propriétés nommées sont en outre attribuées par un jeu de propriétés et un long ID (capot), qui est un entier non signé de 32 bits ou une chaîne. Un jeu de propriétés est un GUID qui identifie un groupe de propriétés nommés avec un rôle similaire. Le jeu de propriétés et le nom capot ou chaîne sont utilisés pour obtenir ou définir la propriété nommée.
  
### <a name="property-type"></a>Type de propriété

À part relatives aux identificateurs, une propriété est attribuée à un type de données qui spécifie le type de valeurs autorisées pour cette propriété.
  
Pour obtenir les propriétés de type chaîne, en fonction de la prise en charge Unicode dans la plate-forme sous-jacente, la propriété peut être de type PT_STRING8 (chaîne null se terminant par le caractère 8 bits) ou PT_UNICODE (chaîne Unicode terminée). Une propriété peut être définie avec le type de PT_TSTRING, et en fonction des paramètres de compilation PT_TSTRING valeur par défaut est une chaîne Unicode pour les plateformes qui prennent en charge Unicode, ou une chaîne PT_STRING8 pour les plateformes qui prennent en charge ANSI ou DBCS. Il est courant qu’une propriété de type chaîne est identifié par trois noms similaires, telles que **PR_ACCOUNT**, **PR_ACCOUNT_A**et **PR_ACCOUNT_W**, qui sont du type PT_TSTRING, PT_STRING8 et PT_UNICODE respectivement.
  
Pour plus d’informations sur les types de propriétés et les macros liées à des types, consultez le fichier d’en-tête MAPI Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identification des propriétés similaires

Dans le paysage de propriété MAPI en cours, il n’est pas rare de trouver qu’une propriété a été exposée sous différents noms de propriétés qui sont définis avec le même identificateur de propriété. Par exemple, les propriétés balisées, **PR_BUSINESS2_TELEPHONE_NUMBER** et **PR_OFFICE2_TELEPHONE_NUMBER**, sont définies dans Mapitags.h d’avoir le même identificateur de la propriété et le type. Étroitement liées à ces deux propriétés sont :
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Les propriétés en utilisant le suffixe « _A » sont de type PT_STRING8, et celles avec le suffixe « _W » sont de type PT_UNICODE.
  
Le but d’une propriété canonique, **PidTagBusiness2TelephoneNumber** dans cet exemple, est de faciliter le référencement des propriétés MAPI étroitement liées à l’aide d’un identificateur et de manière cohérente (en utilisant le préfixe « Pid ») sur tous les MAPI Propriétés. Pour trouver les propriétés MAPI réelles qui représente une propriété canonique, voir [Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md). Pour trouver la propriété canonique qui est associée à une propriété MAPI, voir [Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Prise en charge MAPI de noms de propriété canonique

Étant donné que les propriétés canoniques ne sont pas des propriétés réel et ne sont pas définies dans les fichiers d’en-tête MAPI, vous devez utiliser pas les noms de propriété canonique dans le code ; au lieu de cela, vous devez continuer à utiliser les noms de propriété MAPI exactes dans le code. Par exemple, vous pouvez faire référence **PR_BUSINESS2_TELEPHONE_NUMBER** et **PR_OFFICE2_TELEPHONE_NUMBER** en dehors du code en tant que **PidTagBusiness2TelephoneNumber**et utiliser les **PR_BUSINESS2_TELEPHONE_NUMBER** ou **PR_OFFICE2_ TELEPHONE_NUMBER** dans le code. 
  
Si vous devez utiliser des noms de propriété canonique dans votre code, vous devez d’abord définir les dans vos propres fichiers d’en-tête.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Noms de propriété canonique et les spécifications du protocole Exchange

Nom canonique est mentionnés dans les spécifications de protocole de Microsoft Exchange Server qui sont utilisées par Exchange Server pour communiquer avec d’autres produits Microsoft. Pour plus d’informations sur les propriétés de l’objet message référencé par les spécifications du protocole Exchange, voir [[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[Balises de propriété MAPI](mapi-property-tags.md)
  
[Vue d’ensemble d’identificateur de propriété MAPI](mapi-property-identifier-overview.md)
  
[Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md)

