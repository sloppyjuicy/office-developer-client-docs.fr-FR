---
title: Vue d’ensemble des types de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ce3cd37247f37c4e70adb07769f00b2df07307a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784674"
---
# <a name="mapi-property-type-overview"></a>Vue d’ensemble des types de propriété MAPI
  
**S’applique à**: Outlook 
  
Types de propriété sont des constantes définies par MAPI dans le MAPIDEFS. Fichier d’en-tête H qui indiquent le type de données sous-jacent d’une valeur de propriété. Toutes les propriétés, qu’ils sont définis par MAPI, d’applications clientes ou par les fournisseurs de service, utilisent une de ces types. 
  
Types de propriété suivent une convention d’affectation de noms similaire à celui utilisé pour les balises de propriété. Beaucoup d’autres types de propriété ont une valeur unique et plusieurs valeurs version. Propriétés à valeurs uniques contient une valeur de son type tel qu’un nombre entier unique ou une chaîne de caractères. La constante permet de représenter une propriété à valeur unique comporte deux parties : le préfixe PT_ et une chaîne décrivant le type réel, tels que LONG ou STRING8. 
  
Propriétés à plusieurs valeurs contient plusieurs valeurs de son type. Contrairement aux tableaux variants OLE, chaque valeur dans une propriété à valeurs multiples est du même type. La constante utilisée pour représenter les propriétés à valeurs multiples est créée en combinant l’indicateur MV_FLAG avec la constante correspondant de valeur de type single qui représente le type de base. Il existe trois parties : le préfixe PT_ suivi MV_ suivi d’une chaîne qui décrit le type. Par exemple, le type d’une propriété contenant plusieurs entiers est PT_MV_LONG et pour plusieurs chaînes de caractères est PT_MV_STRING8.
  
L’illustration suivante montre la structure d’une structure [SPropValue](spropvalue.md) pour décrire un entier de plusieurs valeurs, une propriété de type PT_MV_LONG. Le membre de la **valeur** est étendu pour inclure le nombre de valeurs de type integer dans la propriété et un pointeur vers un tableau de ces valeurs. 
  
**Propriétés à plusieurs valeurs**
  
![Propriétés à plusieurs valeurs] (media/amapi_12.gif "Propriétés à plusieurs valeurs")
  
Bien que prise en charge de plusieurs valeurs propriétés est facultative, MAPI recommande que les clients et les fournisseurs de services prennent en charge les deux types de propriétés car cela permet tel davantage d’interactions entre les composants compatible MAPI.
  
L’illustration suivante répertorie toutes les constantes de type de propriété différentes, indiquant où ils sont stockés dans une structure **SPropValue** . La taille du membre de la **valeur** dépend du type particulier. Notez que tous les types de valeur unique équivalents plusieurs valeurs. 
  
**Constantes de type de propriété**
  
![Constantes de type de propriété] (media/amapi_11.gif "Constantes de type de propriété")
  
Clients et les fournisseurs de services de travailler avec une propriété doivent suivre deux étapes :
  
1. Déterminer si la propriété est disponible ou non disponible.
    
2. Si elle est disponible, récupérez la valeur de propriété.
    
Parfois un client ou fournisseur de services ne vérifiez l’existence d’une propriété. d’autres cas, il est nécessaire rechercher une valeur spécifique. Par exemple, les fournisseurs de transport ont trois différents cours d’action pour le traitement du **PR\_SEND_RICH_INFO** propriété ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), une valeur de type Boolean qui indique si un message doit être transmis avec texte mis en forme. Si **PR\_SEND_RICH_INFO** est défini sur TRUE, le fournisseur de transport transmet le texte mis en forme. Si elle est définie sur FALSE, le texte mis en forme est ignoré avant la transmission. Si **PR_SEND_RICH_INFO** n’est pas disponible, le fournisseur de transport suit son cours par défaut de l’action, quelle que soit autrement dit pour le fournisseur particulier. 
  
MAPI définit un type de propriété spécifique, PT_UNSPECIFIED, qui a un client ou fournisseur de services peut utiliser pour récupérer une propriété lors de la propriété type est inconnu. Pour récupérer une propriété insu avance de son type, un client ou fournisseur de services appelle la méthode d’un objet [IMAPIProp::GetProps](imapiprop-getprops.md) et transmet une balise de propriété d’identificateur de la propriété et le type de propriété PT_UNSPECIFIED. **GetProps** renvoie une structure [SPropValue](spropvalue.md) pour la propriété, en remplaçant PT_UNSPECIFIED par le type approprié. Fournisseurs de services de mise en œuvre **GetProps** sont requis pour prendre en charge PT_UNSPECIFIED. 
  
Certains objets MAPI prennent en charge les propriétés qui sont eux-mêmes des objets. Propriétés de l’objet ont le type PT_OBJECT. Au lieu d’utiliser **IMAPIProp::GetProps** pour accéder à ces propriétés, les clients et les fournisseurs de services généralement utilisateur soit la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , spécifiez l’interface appropriée pour l’accès ou une méthode sur l’objet prise en charge de la propriété. 
  
Étant donné que l’accès à la valeur de propriété d’un objet implique l’utilisation d’une des interfaces de l’objet, **GetProps** n’est pas appropriée. Avec **GetProps**, l’appelant accède à valeur d’une propriété à travers une structure **SPropValue** . Avec **IMAPIProp::OpenProperty**, l’appelant récupère un pointeur vers une interface qui peut accéder à l’objet. **OpenProperty** peut toujours être utilisé pour récupérer une propriété d’objet. L’autre option, en appelant une méthode sur l’objet, n’est pas disponible avec chaque propriété de l’objet. 
  
Par exemple, chaque dossier prend en charge deux tables, une table de hiérarchie et une table des matières. Ces tables sont des propriétés du dossier. les balises de propriété sont **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Les tableaux sont des objets qui nécessitent l’interface **IMAPITable** pour l’accès. Un client peut appeler la méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier pour accéder à la table de hiérarchie, méthode de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier pour accéder à la table des matières ou le dossier [IMAPIProp::OpenProperty ](imapiprop-openproperty.md)méthode pour accéder à une table. Pour appeler **OpenProperty**, un client transmet la balise de propriété pour la propriété en tant que le premier paramètre et un identificateur d’interface pour l’interface à utiliser pour l’accès en tant que deuxième paramètre. Ces paramètres serait **PR_CONTAINER_HIERARCHY** ou **PR_CONTAINER_CONTENTS** et **IID_IMAPITable**.
  
Pour obtenir une liste complète des types de valeur unique et plusieurs valeurs de propriété, voir [Types de propriété](property-types.md). 
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de la propri�t� MAPI](mapi-property-overview.md)

