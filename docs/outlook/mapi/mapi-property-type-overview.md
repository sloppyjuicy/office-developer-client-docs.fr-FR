---
title: Vue d’ensemble du type de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438196"
---
# <a name="mapi-property-type-overview"></a>Vue d’ensemble du type de propriété MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les types de propriétés sont des constantes définies par MAPI dans MAPIDEFS. Fichier d’en-tête H qui indique le type de données sous-jacent d’une valeur de propriété. Toutes les propriétés, qu’elles soient définies par MAPI, par des applications clientes ou par des fournisseurs de services, utilisent l’un de ces types. 
  
Les types de propriété suivent une convention d’attribution de noms similaire à celle utilisée pour les balises de propriété. De nombreux types de propriétés ont à la fois une version à valeur unique et une version à valeurs multiples. Les propriétés à valeur unique contiennent une valeur de son type, par exemple un seul nombre d’nombres ou une chaîne de caractères. La constante utilisée pour représenter une propriété à valeur unique est en deux parties : le préfixe PT_ et une chaîne décrivant le type réel, telle que LONG ou STRING8. 
  
Les propriétés à valeurs multiples contiennent plusieurs valeurs de son type. Contrairement aux tableaux de variantes OLE, chaque valeur d’une propriété à valeurs multiples est du même type. La constante utilisée pour représenter les propriétés à valeurs multiples est créée en combinant l’indicateur MV_FLAG avec la constante de valeur unique correspondante représentant le type de base. Il existe trois parties : le préfixe PT_ suivi de MV_ suivi d’une chaîne qui décrit le type. Par exemple, le type d’une propriété contenant plusieurs nombres d’PT_MV_LONG et pour plusieurs chaînes de caractères est PT_MV_STRING8.
  
L’illustration suivante montre la structure d’une structure [SPropValue](spropvalue.md) pour décrire un nombre entière à valeurs multiples, une propriété de type PT_MV_LONG. Le **membre Value** est étendu pour inclure le nombre de valeurs entières dans la propriété et un pointeur vers un tableau de ces valeurs. 
  
**Propriétés à plusieurs valeurs**
  
![Propriétés à valeurs multiples](media/amapi_12.gif "Propriétés à valeurs multiples")
  
Bien que la prise en charge des propriétés à valeurs multiples soit facultative, MAPI recommande que les clients et les fournisseurs de services les prise en charge des deux types de propriétés, car cela permet une meilleure interaction entre les composants compatibles MAPI.
  
L’illustration suivante répertorie toutes les différentes constantes de type de propriété, montrant où elles sont stockées dans une structure **SPropValue.** La taille du membre **Value** dépend du type particulier. Notez que tous les types à valeur unique n’ont pas d’équivalents à valeurs multiples. 
  
**Constantes de type de propriété**
  
![Constantes de type de propriété Constantes](media/amapi_11.gif "de type propriété")
  
Les clients et les fournisseurs de services qui travaillent avec une propriété doivent suivre deux étapes :
  
1. Déterminez si la propriété est disponible ou non.
    
2. Si disponible, récupérez la valeur de la propriété.
    
Parfois, un client ou un fournisseur de services doit uniquement vérifier l’existence d’une propriété ; d’autres fois, il est nécessaire de vérifier une valeur spécifique. Par exemple, les fournisseurs de transport ont trois procédures différentes pour traiter la propriété **\_ PR SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), une valeur booléen qui indique si un message doit être transmis avec du texte formaté. Si **pr \_ SEND_RICH_INFO** est définie sur TRUE, le fournisseur de transport transmet le texte mis en forme. Si elle est définie sur FALSE, le texte mis en forme est ignoré avant la transmission. Si **PR_SEND_RICH_INFO** n’est pas disponible, le fournisseur de transport suit sa ligne de route par défaut, quelle qu’elle soit pour le fournisseur particulier. 
  
MAPI définit un type de propriété spécial, PT_UNSPECIFIED, qu’un client ou un fournisseur de services peut utiliser pour récupérer une propriété lorsque le type de propriété est inconnu. Pour récupérer une propriété sans connaissance préalable de son type, un client ou un fournisseur de services appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet et transmet une balise de propriété composé de l’identificateur de la propriété et du type de propriété PT_UNSPECIFIED. **GetProps renvoie** une structure [SPropValue](spropvalue.md) pour la propriété, en remplaçant PT_UNSPECIFIED par le type approprié. Les fournisseurs de services implémentant **GetProps** sont requis pour prendre en charge PT_UNSPECIFIED. 
  
Certains objets MAPI supportent des propriétés qui sont elles-mêmes des objets. Les propriétés d’objet ont le type PT_OBJECT. Au lieu d’utiliser **IMAPIProp::GetProps** pour accéder à ces propriétés, les clients et fournisseurs de services utilisent généralement la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en spécifiant l’interface appropriée pour l’accès, ou une méthode sur l’objet qui prend en charge la propriété. 
  
Étant donné que l’accès à la valeur d’une propriété d’objet implique l’utilisation de l’une des interfaces de l’objet, **GetProps** n’est pas approprié. Avec **GetProps,** l’appelant accède à la valeur d’une propriété via une structure **SPropValue.** Avec **IMAPIProp::OpenProperty,** l’appelant récupère un pointeur vers une interface qui peut accéder à l’objet. **OpenProperty peut** toujours être utilisé pour récupérer une propriété d’objet. L’autre option, l’appel d’une méthode sur l’objet, n’est pas disponible avec toutes les propriétés d’objet. 
  
Par exemple, chaque dossier prend en charge deux tables, une table hiérarchique et une table des matières. Ces tableaux sont des propriétés du dossier ; leurs balises de propriété **sont PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Les tableaux sont des objets qui nécessitent l’interface **IMAPITable** pour l’accès. Un client peut appeler la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier pour accéder à la table hiérarchique, la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier pour accéder à la table des matières ou la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du dossier pour accéder à l’une ou l’autre table. Pour appeler **OpenProperty,** un client transmet la balise de propriété pour la propriété en tant que premier paramètre et un identificateur d’interface pour l’interface à utiliser pour l’accès en tant que deuxième paramètre. Ces paramètres sont **PR_CONTAINER_HIERARCHY** ou **PR_CONTAINER_CONTENTS** et **IID_IMAPITable**.
  
Pour obtenir la liste complète des types de propriétés à valeur unique et à valeurs multiples, voir [Types de propriétés.](property-types.md) 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

