---
title: ButtonFace, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
ms.localizationpriority: medium
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.
ms.openlocfilehash: 9933d86832fed31668482a9209092f37d1a1eb56
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381102"
---
# <a name="buttonface-cell-action-tags-section"></a>ButtonFace, cellule (section Action Tags)

Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».
  
## <a name="remarks"></a>Remarques

La chaîne contenue dans la cellule ButtonFace représente l'ID d'une image de bouton Microsoft Office. Une valeur de 0 (zéro) ou vide par défaut pour le bouton d’informations « i » de la balise d’action standard ![Bouton d’informations « i » de la balise d’action standard](media/InfoPS_ZA10180114.gif).
  
Les ID utilisables dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d'un objet **CommandBarButton**. Pour plus d’informations sur ces ID, recherchez « Working with command bar button images » sur MSDN.
  
Pour obtenir une référence à la cellule ButtonFace par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom* . ButtonFace où SmartTags. *nom*. est le nom de la ligne de balise d’action.  <br/> |

Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visSmartTagButtonFace** <br/> |
