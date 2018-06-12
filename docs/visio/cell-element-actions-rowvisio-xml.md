---
title: Élément de cellule (ligne Actions) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou action de la balise.
ms.openlocfilehash: d0f103e6f241a7982bcc2663752d9338cf4c3eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788178"
---
# <a name="cell-element-actions-row-visio-xml"></a>Élément de cellule (ligne Actions) (« Visio XML »)

Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou action de la balise.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.XML, maître # .xml, pages.xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Section Actions)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou action de la balise.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD : String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur de **E** est la valeur actuelle (chaîne message d’erreur) ; la valeur de l’attribut de **V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |XSD : String  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir une des chaînes suivantes :  <br/>  « (une formule) » si la formule existe localement  <br/>  `No Formula`Si la formule est localement supprimée ou bloquée  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Représente le nom de la cellule de feuille ShapeSheet.  <br/> |Le nom de la cellule de feuille ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente une unité de mesure par défaut est la liste de distribution.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |La valeur de la cellule de feuille ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Note

L’attribut **N** de cet élément de **cellule** doit être un ensemble limité de valeurs qui correspondent à des cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Action  <br/> |Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.  <br/> |[Action, cellule (section Actions)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indique si un séparateur est inséré dans le menu au-dessus de cette action.  <br/> |[BeginGroup, cellule (section Actions)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.  <br/> |[ButtonFace, cellule (section Actions)](buttonface-cell-actions-section.md) <br/> |
|Activée  <br/> |Indique si une option est cochée dans le menu contextuel ou de balise d’action.  <br/> |[Checked, cellule (section Actions)](checked-cell-actions-section.md) <br/> |
|Désactivé  <br/> |Indique si une option d’un menu contextuel ou de balise d’action est désactivée.  <br/> |[Disabled, cellule (section Actions)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.  <br/> |[FlyoutChild, cellule (Section Actions)](flyoutchild-cell-actions-section.md) <br/> |
|Invisible  <br/> |Indique si l’action est visible dans le menu contextuel ou de balise d’action.  <br/> |[Invisible, cellule (section Actions)](invisible-cell-actions-section.md) <br/> |
|Menu  <br/> |Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.  <br/> |[Menu, cellule (section Actions)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.  <br/> |[ReadOnly, cellule (section Actions)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.  <br/> |[SortKey, cellule (Section Actions) SortKey, cellule (Section Actions)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Contient le nom de la balise d’action à laquelle cette action est associée.  <br/> |[TagName, cellule (section Actions)](tagname-cell-actions-section.md) <br/> |
   

