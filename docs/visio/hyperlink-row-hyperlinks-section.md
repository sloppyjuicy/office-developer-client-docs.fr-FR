---
title: Hyperlink, ligne (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.
ms.openlocfilehash: 99295838f5d1860e3c34cf4e37866eb477fe81ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788796"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Hyperlink, ligne (section Hyperlinks)

Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.
  
Les lignes Hyperlink sont nommées Hyperlink. *nom* et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Description](description-cell-hyperlinks-section.md) <br/> |Chaîne de texte descriptive d'un lien hypertexte  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |Adresse URL, nom de fichier MS-DOS ou chemin UNC à lancer  <br/> |
|[Sous-adresse](subaddress-cell-hyperlinks-section.md) <br/> |Emplacement dans le document cible vers lequel le lien se fait  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Chaîne qui transmet les informations à utiliser pour la résolution d'une URL  <br/> |
|[Cadre](frame-cell-hyperlinks-section.md) <br/> |Nom d'un cadre à cibler lorsque Microsoft Office Visio est ouvert en tant que document actif dans un conteneur ActiveX. Par défaut, cette chaîne est vide.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Détermine l'ordre d'apparition des liens hypertexte dans le menu contextuel.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre. Si cette cellule a la valeur TRUE, la page, le document ou le site Web est ouvert dans une nouvelle fenêtre. Par défaut, la valeur est FALSE.  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |Lien hypertexte par défaut d'une forme ou d'une page  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Indique si le lien hypertexte apparaît dans le menu contextuel.  <br/> |
   
## <a name="remarks"></a>Notes

 Vous pouvez ajouter autant de lien hypertexte.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter des liens hypertexte à une section Hyperlinks existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer ces cellules par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour attribuer des noms explicites au lien hypertexte. *nom de* lignes, cliquez sur la ligne, puis tapez un nom tel que *Marketing* , par exemple, pour créer le nom de ligne Hyperlink.Marketing. Vous pouvez ensuite référencer la cellule Description à l’aide de Hyperlink.Marketing.Description. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

