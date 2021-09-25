---
title: Afficher les tableaux
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fa65f150639a0604ee84f038c92cec0b0a10e43e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588169"
---
# <a name="display-tables"></a>Afficher les tableaux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un tableau d’affichage décrit comment afficher un type spécifique de boîte de dialogue : une ou plusieurs pages de propriétés à onglets sont dédiées à l’affichage et éventuellement à la modification d’une ou de plusieurs propriétés. Une implémentation d’interface [IMAPIProp : IUnknown](imapipropiunknown.md) est associée à chaque tableau d’affichage. **L’implémentation IMAPIProp** conserve les données de propriété présentées dans la boîte de dialogue. 
  
Les lignes d’un tableau d’affichage représentent les contrôles, ou objets de l’interface utilisateur, qui sont affichés dans la boîte de dialogue. MAPI définit de nombreux types de contrôles, certains avec des valeurs statiques et d’autres avec des valeurs dynamiques qu’un utilisateur peut modifier. La plupart des contrôles peuvent être associés à des propriétés conservées avec **l’implémentation IMAPIProp.** Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mise à jour. 
  
Les fournisseurs de services implémentent des tables d’affichage et l’interface **IMAPIProp.** La création d’un tableau d’affichage est similaire à l’écriture d’un programme avec un langage de script. Les fournisseurs de services peuvent créer un tableau d’affichage en : 
  
- Appel de [la fonction BuildDisplayTable.](builddisplaytable.md) 
    
    - Ou -
    
- Inclure du code personnalisé qui remplit la table d’affichage directement à l’aide d’un objet de données de table , un objet qui prend en charge l’interface [ITableData : IUnknown.](itabledataiunknown.md) 
    
La **fonction BuildDisplayTable** combine les informations des structures de tableau d’affichage avec les éléments visuels d’une ressource de boîte de dialogue pour créer des lignes de tableau d’affichage. La fonction renvoie un pointeur vers une implémentation d’interface [IMAPITable : IUnknown](imapitableiunknown.md) et, si nécessaire, un pointeur vers une implémentation d’interface **ITableData.** 
  
**L’utilisation de BuildDisplayTable** pour créer un tableau d’affichage est simple et facilite la maintenance lorsque les éléments visuels de la modification d’affichage. Toutefois, les fournisseurs de services qui préfèrent ne pas utiliser **BuildDisplayTable** peuvent créer un tableau d’affichage avec du code personnalisé qui utilise les méthodes de **ITableData**. Par exemple, les fournisseurs de services qui ont une structure de modèle existante pour leurs pages de propriétés peuvent vouloir créer du code personnalisé plutôt que d’utiliser **BuildDisplayTable**.
  
Les fournisseurs de services peuvent implémenter l’interface de propriétés de leur tableau d’affichage de différentes manières. Cela comprend :
  
- Fourniture d’une [implémentation IMAPIProp : IUnknown](imapipropiunknown.md) standard. 
    
- Fourniture d’une implémentation **IMAPIProp** wrapped qui inclut un traitement spécial avant d’effectuer les appels standard. 
    
- Fourniture [d’une implémentation IPropData : IMAPIProp.](ipropdataimapiprop.md) 
    
Le type d’implémentation dépend des caractéristiques des données à afficher et du fournisseur de services responsable. Par exemple, s’il existe une relation implicite entre les données dans deux contrôles d’édition et qu’un des contrôles change, l’implémentation **IMAPIProp** doit modifier la valeur de l’autre contrôle de manière appropriée. 
  
Les tableaux d’affichage ont les propriétés suivantes dans leur jeu de colonnes requis :
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** et **PR_YPOS** les coordonnées X et Y du coin supérieur gauche du contrôle. Les unités horizontales sont égales à 1/4 de l’unité de largeur de base de la boîte de dialogue . les unités verticales sont 1/8 de l’unité de hauteur de base de la boîte de dialogue. Windows calcule les unités de base de la boîte de dialogue actuelle à partir de la hauteur et de la largeur de la police système actuelle. Les coordonnées sont relatives à l’origine de la zone de page de propriétés. La taille des pages de propriétés est limitée à environ 200 par 180 unités de boîte de dialogue. 
  
 **PR_DELTAX** et **PR_DELTAY** sont la largeur et la hauteur du contrôle. Valeurs ULONG. Les unités de largeur sont égales à 1/4 de l’unité de largeur de base de la boîte de dialogue . les unités de hauteur sont 1/8 de l’unité de hauteur de base de la boîte de dialogue. Les coordonnées sont relatives à l’origine du contrôle. 
  
Les quatre autres propriétés décrivent différentes caractéristiques du contrôle. **PR_CONTROL_TYPE** indique le type de contrôle. MAPI définit douze types de contrôles, chacun avec un ensemble d’attributs différent. Ces attributs sont décrits dans la propriété flags, **PR_CONTROL_FLAGS**. Il peut s’agir, par exemple, d’un contrôle modifiable ou obligatoire. 
  
La structure de contrôle, **PR_CONTROL_STRUCTURE,** contient des informations pertinentes pour le type particulier de contrôle. Chaque type de contrôle est décrit avec une structure différente. Par exemple, les contrôles d’édition sont décrits avec la structure [DTBLEDIT.](dtbledit.md) Les structures **DTBLEDIT** contiennent des membres qui indiquent le nombre de caractères et des types spécifiques de caractères qui peuvent être placés sur le contrôle et une balise de propriété qui identifie la propriété dont la valeur doit être affichée dans le contrôle. **PR_CONTROL_STRUCTURE** est stockée en tant que propriété binaire. 
  
**L’identificateur de PR_CONTROL_ID**, identifie de manière unique le contrôle dans la boîte de dialogue décrite par le tableau d’affichage. **PR_CONTROL_ID** est définie à partir des valeurs placées dans les membres  *lpbNotif*  et  *cbNotif*  de la structure [DTCTL](dtctl.md) utilisée par **BuildDisplayTable** pour créer le tableau d’affichage. Étant donné que MAPI combine parfois des tableaux d’affichage, l’identificateur **dans PR_CONTROL_ID** doit toujours être unique. En règle générale, les fournisseurs affectent une structure [GUID](guid.md) **PR_CONTROL_ID** pour garantir son unicité. La **PR_CONTROL_ID** est incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) lorsqu’une notification de tableau d’affichage est générée. 
  
Pour plus d’informations sur les tableaux d’affichage, voir [Implémentation de tableau](display-table-implementation.md) d’affichage et À propos des [notifications de tableau d’affichage.](about-display-table-notifications.md) 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

