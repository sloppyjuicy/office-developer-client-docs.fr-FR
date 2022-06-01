---
title: Afficher les tables
description: Une table d’affichage explique comment afficher un type de boîte de dialogue , avec une ou plusieurs pages de propriétés à onglets dédiées à l’affichage ou à la modification d’une ou plusieurs propriétés.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
ms.openlocfilehash: c373b616f5fcfbd2ae597174943f3e62144d46a4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817108"
---
# <a name="display-tables"></a>Afficher les tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016
  
Un tableau d’affichage explique comment afficher un type spécifique de boîte de dialogue , une ou plusieurs pages de propriétés à onglets dédiées à l’affichage et éventuellement à la modification d’une ou de plusieurs propriétés. Une implémentation d’interface [IMAPIProp : IUnknown](imapipropiunknown.md) est associée à chaque table d’affichage. L’implémentation **IMAPIProp** conserve les données de propriété présentées dans la boîte de dialogue.
  
Les lignes d’une table d’affichage représentent les contrôles, ou objets d’interface utilisateur, qui sont affichés dans la boîte de dialogue. MAPI définit de nombreux types de contrôles, certains avec des valeurs statiques et d’autres avec des valeurs dynamiques qu’un utilisateur peut modifier. La plupart des contrôles peuvent être associés à des propriétés gérées avec l’implémentation **IMAPIProp** . Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mise à jour.
  
Les fournisseurs de services implémentent des tables d’affichage et l’interface **IMAPIProp** . La création d’une table d’affichage est similaire à l’écriture d’un programme avec un langage de script. Les fournisseurs de services peuvent créer une table d’affichage en :
  
- Appel de la fonction [BuildDisplayTable](builddisplaytable.md) .

    - Ou -

- Y compris le code personnalisé qui remplit la table d’affichage directement à l’aide d’un objet de données de table , un objet qui prend en charge l’interface [ITableData : IUnknown](itabledataiunknown.md) .

La fonction **BuildDisplayTable** combine les informations des structures de table d’affichage avec les éléments visuels d’une ressource de boîte de dialogue pour générer des lignes de table d’affichage. La fonction retourne un pointeur vers une implémentation d’interface [IMAPITable : IUnknown](imapitableiunknown.md) et, si nécessaire, un pointeur vers une implémentation d’interface **ITableData** .
  
**L’utilisation de BuildDisplayTable** pour créer une table d’affichage est simple et facilite la maintenance lorsque des éléments visuels de l’affichage changent. Toutefois, les fournisseurs de services qui préfèrent ne pas utiliser **BuildDisplayTable** peuvent créer une table d’affichage avec du code personnalisé qui utilise les méthodes **d’ITableData**. Par exemple, les fournisseurs de services qui ont une structure de modèle existante pour leurs pages de propriétés peuvent souhaiter créer du code personnalisé plutôt que d’utiliser **BuildDisplayTable**.
  
Il existe différentes façons dont les fournisseurs de services peuvent implémenter l’interface de propriété pour leur table d’affichage. Cela inclut ce qui suit :
  
- Fourniture d’une implémentation [IMAPIProp : IUnknown](imapipropiunknown.md) standard.
    
- Fourniture d’une implémentation **IMAPIProp** encapsulée qui inclut un traitement spécial avant d’effectuer les appels standard.
    
- Fourniture d’une implémentation [IPropData : IMAPIProp](ipropdataimapiprop.md) .
    
Le type d’implémentation dépend des caractéristiques des données à afficher et du fournisseur de services responsable. Par exemple, s’il existe une relation implicite entre les données dans deux contrôles d’édition et si l’un des contrôles change, l’implémentation **IMAPIProp** doit modifier la valeur de l’autre contrôle de manière appropriée.
  
Les tables d’affichage ont les propriétés suivantes dans leur ensemble de colonnes requis :
  
||Valeur |
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |

 **PR_XPOS** et **PR_YPOS** spécifiez les coordonnées X et Y du coin supérieur gauche du contrôle. Les unités horizontales sont 1/4 de l’unité de largeur de base du dialogue ; les unités verticales sont égales à 1/8 de l’unité de hauteur de base du dialogue. Windows calcule les unités de base de dialogue actuelles à partir de la hauteur et de la largeur de la police système actuelle. Les coordonnées sont relatives à l’origine de la zone de page de propriétés. La taille des pages de propriétés est limitée à environ 200 par 180 unités de dialogue.
  
 **PR_DELTAX** et **PR_DELTAY** sont la largeur et la hauteur du contrôle. Il s’agit de valeurs ULONG. Les unités de largeur sont égales à 1/4 de l’unité de largeur de base du dialogue ; les unités de hauteur sont égales à 1/8 de l’unité de hauteur de base du dialogue. Les coordonnées sont relatives à l’origine du contrôle.
  
Les quatre autres propriétés décrivent différentes caractéristiques du contrôle. **PR_CONTROL_TYPE** indique le type de contrôle. MAPI définit douze types de contrôles, chacun avec un ensemble d’attributs différent. Ces attributs sont décrits dans la propriété flags, **PR_CONTROL_FLAGS**. Les exemples d’attributs incluent la question de savoir si un contrôle est modifiable ou requis.
  
La structure de contrôle, **PR_CONTROL_STRUCTURE**, contient des informations pertinentes pour le type particulier de contrôle. Chaque type de contrôle est décrit avec une structure différente. Par exemple, les contrôles d’édition sont décrits avec la structure [DTBLEDIT](dtbledit.md) . **Les structures DTBLEDIT** contiennent des membres qui répertorient le nombre et les types spécifiques de caractères qui peuvent être placés sur le contrôle et une balise de propriété qui identifie la propriété dont la valeur doit être affichée dans le contrôle. **PR_CONTROL_STRUCTURE** est stocké en tant que propriété binaire.
  
L’identificateur de contrôle, **PR_CONTROL_ID**, identifie de façon unique le contrôle dans la boîte de dialogue décrite par la table d’affichage. **PR_CONTROL_ID** est définie à partir des valeurs placées dans les membres *lpbNotif* et *cbNotif* de la structure [DTCTL](dtctl.md) utilisées par **BuildDisplayTable** pour créer la table d’affichage. Étant donné que MAPI combine parfois des tables d’affichage, l’identificateur dans **PR_CONTROL_ID** doit toujours être unique. En règle générale, les fournisseurs attribuent une structure [GUID](guid.md) à **PR_CONTROL_ID** pour garantir son unicité. La propriété **PR_CONTROL_ID** est incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) lorsqu’une notification de table d’affichage est générée.
  
Pour plus d’informations sur les tables d’affichage, consultez [Implémentation de table d’affichage](display-table-implementation.md) et [À propos des notifications de table d’affichage](about-display-table-notifications.md).
  
## <a name="see-also"></a>Voir aussi

[MAPI Tables](mapi-tables.md)
