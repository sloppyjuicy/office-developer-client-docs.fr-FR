---
title: Hyperlink, ligne (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
ms.localizationpriority: medium
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.
ms.openlocfilehash: 6c120082810b92aaa78e4560bb5df4fa1f3b556a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787183"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Hyperlink, ligne (section Hyperlinks)

Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.
  
Les lignes Hyperlink sont nommées Hyperlink. *et*  contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Description](description-cell-hyperlinks-section.md) <br/> |Chaîne de texte descriptive d'un lien hypertexte |
|[Address](address-cell-hyperlinks-section.md) <br/> |Adresse URL, nom de fichier MS-DOS ou chemin UNC à lancer |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Emplacement dans le document cible vers lequel le lien se fait |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Chaîne qui transmet les informations à utiliser pour la résolution d'une URL |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Nom d'un cadre à cibler lorsque Microsoft Office Visio est ouvert en tant que document actif dans un conteneur ActiveX. Par défaut, cette chaîne est vide. |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Détermine l'ordre d'apparition des liens hypertexte dans le menu contextuel. |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre. Si la valeur est TRUE, ouvre la page liée, le document ou le site web dans une nouvelle fenêtre. Par défaut, la valeur est FALSE. |
|[Par défaut](default-cell-hyperlinks-section.md) <br/> |Lien hypertexte par défaut d'une forme ou d'une page |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Indique si le lien hypertexte apparaît dans le menu contextuel. |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de lignes Hyperlink.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter des liens hypertexte à une section Hyperlinks existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants aux lignes Hyperlink. *name*  rows, click the row, and then type a name such as  *Marketing*  , for example, to create the row name Hyperlink.Marketing. Vous pouvez alors faire référence à la cellule Description en utilisant Hyperlink.Marketing.Description. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

