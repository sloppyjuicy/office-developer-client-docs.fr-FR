---
title: Tables d'affichage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406219"
---
# <a name="display-tables"></a>Tables d'affichage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table d'affichage décrit comment afficher un type spécifique de boîte de dialogue: une ou plusieurs pages de propriétés à onglets dédiées à l'affichage et éventuellement la modification d'une ou plusieurs propriétés. Chaque table d'affichage est une [IMAPIProp:](imapipropiunknown.md) implémentation de l'interface IUnknown. L'implémentation de **IMAPIProp** gère les données de propriété présentées dans la boîte de dialogue. 
  
Les lignes d'une table d'affichage représentent les contrôles, ou objets d'interface utilisateur, qui s'affichent dans la boîte de dialogue. MAPI définit de nombreux types de contrôles, d'autres avec des valeurs statiques et d'autres avec des valeurs dynamiques qu'un utilisateur peut modifier. La plupart des contrôles peuvent être associés à des propriétés gérées à l'aide de l'implémentation **IMAPIProp** . Lorsqu'un utilisateur modifie la valeur d'un contrôle modifiable, la propriété correspondante est mise à jour. 
  
Les fournisseurs de services implémentent les tables d'affichage et l'interface **IMAPIProp** . La création d'une table d'affichage est semblable à l'écriture d'un programme à l'aide d'un langage de script. Les fournisseurs de services peuvent créer un tableau d'affichage en procédant comme suit: 
  
- Appel de la fonction [BuildDisplayTable](builddisplaytable.md) . 
    
    - Des
    
- Y compris le code personnalisé qui remplit la table d'affichage directement à l'aide d'un objet de données de table, un objet qui prend en charge l'interface [ITableData: IUnknown](itabledataiunknown.md) . 
    
La fonction **BuildDisplayTable** combine les informations des structures de tables d'affichage avec les éléments visuels d'une ressource de boîte de dialogue pour créer des lignes de tableau d'affichage. La fonction renvoie un pointeur vers une interface [IMAPITable:](imapitableiunknown.md) l'implémentation de l'interface IUnknown et, si nécessaire, un pointeur vers une implémentation de l'interface **ITableData** . 
  
L'utilisation de **BuildDisplayTable** pour créer une table d'affichage est simple et facilite la maintenance lorsque les éléments visuels de l'affichage changent. Toutefois, les fournisseurs de services qui préfèrent ne pas utiliser **BuildDisplayTable** peuvent créer une table d'affichage avec du code personnalisé qui utilise les méthodes de **ITableData**. Par exemple, les fournisseurs de services qui ont une structure de modèle existante pour leurs pages de propriétés peuvent souhaiter créer du code personnalisé au lieu d'utiliser **BuildDisplayTable**.
  
Il existe plusieurs façons pour les fournisseurs de services d'implémenter l'interface de propriétés pour leur table d'affichage. Ces approches sont les suivantes :
  
- Fourniture d'une norme [IMAPIProp: IUnknown](imapipropiunknown.md) Implementation. 
    
- Fourniture d'une implémentation **IMAPIProp** incluse dans un wrapper qui inclut un traitement spécial avant de passer les appels standard. 
    
- Fourniture d'une [IPropData: IMAPIProp](ipropdataimapiprop.md) Implementation. 
    
Le type d'implémentation dépend des caractéristiques des données à afficher et du fournisseur de services responsable. Par exemple, s'il existe une relation implicite entre les données de deux contrôles d'édition et que l'un des contrôles est modifié, l'implémentation de **IMAPIProp** doit modifier de manière appropriée la valeur de l'autre contrôle. 
  
Les tables d'affichage possèdent les propriétés suivantes dans leur jeu de colonnes obligatoire:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** et **PR_YPOS** spécifient les coordonnées X et Y du coin supérieur gauche du contrôle. Les unités horizontales sont 1/4 de la largeur de la boîte de dialogue unité de base; les unités verticales sont 1/8 de la hauteur de la boîte de dialogue. Windows calcule les unités de base de la boîte de dialogue actuelle à partir de la hauteur et de la largeur de la police système actuelle. Les coordonnées sont relatives à l'origine de la zone de la page de propriétés. La taille des pages de propriétés est limitée à environ 200 par unité de boîte de dialogue 180. 
  
 **PR_DELTAX** et **PR_DELTAY** sont la largeur et la hauteur du contrôle. Il s'agit de valeurs ULONG. Les unités de largeur sont 1/4 de la largeur de la boîte de dialogue unité de base; les unités de hauteur sont 1/8 de la hauteur de la boîte de dialogue. Les coordonnées sont relatives à l'origine du contrôle. 
  
Les quatre autres propriétés décrivent différentes caractéristiques du contrôle. **PR_CONTROL_TYPE** indique le type de contrôle. MAPI définit douze types de contrôles, chacun avec un jeu d'attributs différent. Ces attributs sont décrits dans la propriété Flags, **PR_CONTROL_FLAGS**. Des exemples d'attributs incluent si un contrôle est modifiable ou obligatoire. 
  
La structure de contrôle, **PR_CONTROL_STRUCTURE**, contient des informations relatives au type de contrôle particulier. Chaque type de contrôle est décrit par une structure différente. Par exemple, les contrôles d'édition sont décrits à l'aide de la structure [DTBLEDIT](dtbledit.md) . Les structures **DTBLEDIT** contiennent des membres qui répertorient le nombre de types de caractères spécifiques pouvant être placés sur le contrôle et une balise de propriété qui identifie la propriété dont la valeur doit être affichée dans le contrôle. **PR_CONTROL_STRUCTURE** est stocké sous la forme d'une propriété binaire. 
  
L'identificateur de contrôle, **PR_CONTROL_ID**, identifie de manière unique le contrôle dans la boîte de dialogue décrite par la table d'affichage. **PR_CONTROL_ID** est défini à partir des valeurs placées dans les membres *lpbNotif* et *cbNotif* de la structure [DTCTL](dtctl.md) utilisée par **BuildDisplayTable** pour créer la table d'affichage. Dans la mesure où MAPI combine parfois des tables d'affichage, l'identificateur dans **PR_CONTROL_ID** doit toujours être unique. En règle générale, les fournisseurs affectent une structure de [GUID](guid.md) à **PR_CONTROL_ID** pour en garantir l'unicité. La propriété **PR_CONTROL_ID** est incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) lorsqu'une notification de table d'affichage est générée. 
  
Pour plus d'informations sur les tables d'affichage, voir [Display table Implementation](display-table-implementation.md) et [about Display table notifications](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

