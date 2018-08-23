---
title: Tableaux d’affichage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 738957d7fc9567a2e8202802edebd16cf57fbffd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581642"
---
# <a name="display-tables"></a>Tableaux d’affichage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une table d’affichage explique comment afficher un type spécifique de boîte de dialogue, avec une ou plusieurs pages de propriétés dédiées à afficher et de modifier éventuellement une ou plusieurs propriétés. Associé à chaque table est un [IMAPIProp : IUnknown](imapipropiunknown.md) implémentation de l’interface. L’implémentation **IMAPIProp** gère les données de propriété qui sont présentées dans la boîte de dialogue. 
  
Les lignes dans un affichage de tableau représentent les contrôles ou les objets d’interface utilisateur, qui sont affichés dans la boîte de dialogue. MAPI définit plusieurs types de contrôles, avec des valeurs statiques et certains avec un utilisateur peut modifier les valeurs dynamiques. La plupart des contrôles peut être associé à des propriétés gérées avec l’implémentation **IMAPIProp** . Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mis à jour. 
  
Afficher des tables et l’interface **IMAPIProp** implémentés par les fournisseurs de service. Création d’un tableau de l’affichage est semblable à l’écriture d’un programme avec un langage de script. Fournisseurs de services peuvent créer un tableau d’affichage par : 
  
- L’appel de la fonction [BuildDisplayTable](builddisplaytable.md) . 
    
    - Ou -
    
- Y compris le code personnalisé qui remplit la table d’affichage directement à l’aide d’un objet de données de table, un objet qui prend en charge la [ITableData : IUnknown](itabledataiunknown.md) interface. 
    
La fonction **BuildDisplayTable** combine les informations de structures de table complet avec des éléments visuels à partir d’une ressource de boîte de dialogue pour créer des lignes de tableau d’affichage. La fonction retourne un pointeur vers une [IMAPITable : IUnknown](imapitableiunknown.md) implémentation, de l’interface et, si nécessaire, un pointeur vers une implémentation d’interface **ITableData** . 
  
Pour créer une table de l’affichage à l’aide de **BuildDisplayTable** est simple et facilite la maintenance lors de la modification d’éléments visuels de l’affichage. Toutefois, les fournisseurs de services qui préfèrent ne pas utiliser **BuildDisplayTable** peuvent créer un affichage de tableau avec du code personnalisé qui utilise les méthodes de **ITableData**. Par exemple, les fournisseurs de services qui ont une structure de modèle existante pour les pages de propriétés souhaiterez peut-être créer un code personnalisé au lieu d’utiliser **BuildDisplayTable**.
  
Il existe plusieurs façons de fournisseurs de service peuvent implémenter l’interface de propriété pour leur affichage de la table. Cela inclut :
  
- Fournir une norme [IMAPIProp : IUnknown](imapipropiunknown.md) implémentation. 
    
- Fournir une implémentation **IMAPIProp** encapsulée qui inclut un traitement spécial avant d’effectuer les appels standards. 
    
- Fournir un [IPropData : IMAPIProp](ipropdataimapiprop.md) implémentation. 
    
Le type de mise en œuvre dépend les caractéristiques de l’affichage des données et le fournisseur de services responsables. Par exemple, s’il existe une relation implicite entre les données dans deux contrôles d’édition et un des contrôles change, l’implémentation **IMAPIProp** doit modifier la valeur de l’autre contrôle correctement. 
  
Afficher des tables ont les propriétés suivantes dans leur ensemble de colonnes requises :
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** et **PR_YPOS** spécifient les coordonnées X et Y de l’angle supérieur gauche du contrôle. Les unités horizontales sont 1/4 de l’unité de largeur de base boîte de dialogue ; les unités verticales sont 1/8 de l’unité de base hauteur de boîte de dialogue. Windows calcule les unités de base de dialogue actuel à partir de la hauteur et la largeur de la police système actuelle. Les coordonnées sont par rapport à l’origine de la zone de propriété de page. La taille des pages de propriétés est limitée à environ les unités de boîte de dialogue de 200 par 180. 
  
 **PR_DELTAX** et **PR_DELTAY** sont la largeur et la hauteur du contrôle. Il s’agit des valeurs ULONG. Les unités de largeur sont 1/4 de l’unité de largeur de base boîte de dialogue ; les unités de hauteur sont 1/8 de l’unité de base hauteur de boîte de dialogue. Les coordonnées sont par rapport à l’origine du contrôle. 
  
Les quatre propriétés décrivent les différentes caractéristiques du contrôle. **PR_CONTROL_TYPE** indique le type de contrôle. MAPI définit douze types de contrôles, chacun avec un autre ensemble d’attributs. Ces attributs sont décrits dans la propriété flags, **PR_CONTROL_FLAGS**. Si un contrôle est modifiable ou requis ou non des exemples d’attributs. 
  
La structure de contrôle, **PR_CONTROL_STRUCTURE**, contient des informations pertinentes pour le type de contrôle particulier. Chaque type de contrôle est décrit avec une structure différente. Par exemple, les contrôles d’édition sont décrits avec la structure [DTBLEDIT](dtbledit.md) . Structures **DTBLEDIT** contiennent des membres que le nombre et les types spécifiques de caractères qui peuvent être placées sur le contrôle et une balise de propriété qui identifie la propriété dont la valeur doit être affiché dans le contrôle de liste. **PR_CONTROL_STRUCTURE** est stocké comme une propriété binaire. 
  
L’identificateur du contrôle, **PR_CONTROL_ID**, identifie le contrôle dans la boîte de dialogue décrit dans le tableau d’affichage. **PR_CONTROL_ID** est définie à partir des valeurs placés dans les membres *lpbNotif* et *cbNotif* de la structure [DTCTL](dtctl.md) qui est utilisé par **BuildDisplayTable** pour créer le tableau d’affichage. Étant donné que MAPI combine parfois afficher des tables, l’identificateur dans **PR_CONTROL_ID** doit toujours être unique. En règle générale, les fournisseurs affecter une structure [GUID](guid.md) à **PR_CONTROL_ID** pour garantir son unicité. La propriété **PR_CONTROL_ID** est incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) lorsqu’une notification de table complet est générée. 
  
Pour plus d’informations sur les tables d’affichage, voir [Implémentation de Table afficher](display-table-implementation.md) et [Sur Afficher les Notifications de Table](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

