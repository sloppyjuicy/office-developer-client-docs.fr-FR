---
title: Smart Tags, ligne (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026926
ms.localizationpriority: medium
ms.assetid: 065c6977-c737-a4f4-effa-0fd2c98e8bbf
description: Contient les informations relative à une seule balise d’action associée à une forme ou une page. Une forme ou une page contient une ligne Smart Tags pour chaque balise d’action.
ms.openlocfilehash: cb73907aa6793a3be4afe8b1c62e62eeeb115f91
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379247"
---
# <a name="smart-tags-row-action-tags-section"></a>Smart Tags Row (Action Tags Section)

Contient les informations relative à une seule balise d’action associée à une forme ou une page. Une forme ou une page contient une ligne Smart Tags pour chaque balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».
  
Les lignes Smart Tags sont nommées SmartTags. *et*  contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-action-tags-section.md) <br/> |Position *de coordonnée x*  d’un point dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé. |
|[Y](y-cell-action-tags-section.md) <br/> |Position *de*  coordonnée y d’un point dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé. |
|[TagName](tagname-cell-action-tags-section.md) <br/> |Nom logique de la balise d’action. |
|[X Justify](x-justify-cell-action-tags-section.md) <br/> |Décalage *x*  du bouton de balise d’action par rapport au point défini par les cellules X et Y. |
|[Y Justify](y-justify-cell-action-tags-section.md) <br/> |Décalage *y*  du bouton de balise d’action par rapport au point défini par les cellules X et Y. |
|[DisplayMode](displaymode-cell-action-tags-section.md) <br/> |Détermine quand la balise d’action apparaît. |
|[ButtonFace](buttonface-cell-action-tags-section.md) <br/> |ID de l’image qui apparaît sur la face du bouton de la balise d’action. |
|[Description](description-cell-action-tags-section.md) <br/> |Chaîne descriptive de la balise d’action. |
|[Disabled](disabled-cell-action-tags-section.md) <br/> |Indique si la balise d’action est désactivée. |

## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de lignes SmartTags.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter une balise d’action à une section Smart Tags existante, cliquez avec le bouton droit sur une ligne, puis cliquez sur **Insérer une ligne** dans le menu contextuel.
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants aux lignes Smart Tags. *nom*, cliquez sur la ligne, puis tapez un nom, *Taille*, par exemple, pour créer le nom de ligne Smart Tags.Taille. Vous pouvez alors faire référence à la cellule Description en utilisant Smart Tags.Taille.Description.
  
Le nom de ligne que vous entrez doit être unique dans la section.
  