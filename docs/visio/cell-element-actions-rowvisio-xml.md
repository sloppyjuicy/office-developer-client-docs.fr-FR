---
title: Élément de cellule (ligne actions) («Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Spécifie une propriété d'une action associée à une commande personnalisée dans un menu contextuel ou de balise d'action.
ms.openlocfilehash: 01b81a593de07be8059263d7a6e6538f31ed3be1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356272"
---
# <a name="cell-element-actions-row-visio-xml"></a>Élément de cellule (ligne actions) («Visio XML»)

Spécifie une propriété d'une action associée à une commande personnalisée dans un menu contextuel ou de balise d'action.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Masters. xml, Master #. xml, pages. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de ligne (section actions)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d'une action associée à une commande personnalisée dans un menu contextuel ou de balise d'action.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur **E** est la valeur actuelle (chaîne de message d'erreur); la valeur de l'attribut **V** est la dernière valeur valide.  <br/> |Chaîne de message d'erreur.  <br/> |
|F  <br/> |xsd: String  <br/> |facultatif  <br/> | Représente la formule de l'élément. Cet attribut peut contenir l'une des chaînes suivantes:  <br/>  ' (une formule) 'si la formule existe localement  <br/>  `No Formula`Si la formule est supprimée ou bloquée localement  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Consultez la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente une unité de mesure la valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L'attribut **N** de cet élément de **cellule** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet. RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Value**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Action  <br/> |Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.  <br/> |[Action, cellule (section Actions)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indique si un séparateur est inséré dans le menu au-dessus de cette action.  <br/> |[BeginGroup, cellule (section Actions)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.  <br/> |[ButtonFace, cellule (section Actions)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Indique si une option est cochée dans le menu contextuel ou de balise d’action.  <br/> |[Checked, cellule (section Actions)](checked-cell-actions-section.md) <br/> |
|Désactivé  <br/> |Indique si une option d’un menu contextuel ou de balise d’action est désactivée.  <br/> |[Disabled, cellule (section Actions)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.  <br/> |[FlyoutChild Cell (Actions Section)](flyoutchild-cell-actions-section.md) <br/> |
|Visibilité  <br/> |Indique si l’action est visible dans le menu contextuel ou de balise d’action.  <br/> |[Invisible, cellule (section Actions)](invisible-cell-actions-section.md) <br/> |
|Menu  <br/> |Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.  <br/> |[Menu, cellule (section Actions)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.  <br/> |[ReadOnly, cellule (section Actions)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.  <br/> |[SortKey, cellule (section actions) SortKey, cellule (section actions)](sortkey-cell-actions-section.md) <br/> |
|Nombalise  <br/> |Contient le nom de la balise d’action à laquelle cette action est associée.  <br/> |[TagName, cellule (section Actions)](tagname-cell-actions-section.md) <br/> |
   

