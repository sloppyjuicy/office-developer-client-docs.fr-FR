---
title: ButtonFace, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385479"
---
# <a name="buttonface-cell-action-tags-section"></a>Cellule ButtonFace (section Balises d’action)

Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Notes

La chaîne contenue dans la cellule ButtonFace représente l’ID d’une image de face de bouton Microsoft Office. Une valeur de 0 (zéro) ou vide applique par défaut le bouton d’information « i » standard des balises d’action ![Bouton d’informations sur la balise « i » action standard](media/InfoPS_ZA10180114.gif).
  
Les ID qui peuvent être utilisées dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d’un objet **CommandBarButton** . Pour plus d’informations sur ces codes, recherchez « utilisation des images de boutons de barre de commande » sur MSDN. 
  
Pour obtenir une référence à la cellule ButtonFace par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Balises actives.  *nom* . ButtonFace où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagButtonFace** <br/> |
   

