---
title: ButtonFace, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788183"
---
# <a name="buttonface-cell-actions-section"></a>ButtonFace, cellule (section Actions)

Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Notes

La chaîne contenue dans la cellule ButtonFace représente l'ID d'une image de bouton Microsoft Office. Une valeur de zéro (0) ou vide indique qu'aucune icône ne s'affiche. 
  
Les ID qui peuvent être utilisées dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d’un objet **CommandBarButton** . Pour plus d’informations sur ces codes, recherchez « utilisation des images de boutons de barre de commande » sur MSDN. 
  
Pour obtenir une référence à la cellule ButtonFace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |**Actions**.  *nom* . **ButtonFace** où **Actions**.  *nom* est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où **i** = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionButtonFace** <br/> |
   

