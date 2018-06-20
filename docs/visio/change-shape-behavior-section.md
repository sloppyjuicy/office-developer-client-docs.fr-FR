---
title: Section de comportement de forme de modification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Détermine les propriétés qui sont transférées à partir de la forme ancienne de la forme de remplacement pendant une opération de remplacement. Les valeurs des cellules dans la section comportement de forme de modification de la forme de base forme de remplacement sont lus pendant l’opération de remplacement de forme.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788230"
---
# <a name="change-shape-behavior-section"></a>Section de comportement de forme de modification

Détermine les propriétés qui sont transférées à partir de la forme ancienne de la forme de remplacement pendant une opération de remplacement. Les valeurs des cellules dans la section **Modifier le comportement de la forme** de la forme de base forme de remplacement sont lus pendant l’opération de remplacement de forme. 
  
## <a name="remarks"></a>Remarques

En définissant les cellules dans la section **Modifier le comportement de la forme** , vous pouvez vous assurer que certaines propriétés de la forme de remplacement restent inchangées pendant l’opération de remplacement. Propriétés qui ne sont pas protégées sont mis à jour avec les valeurs de forme local de la forme ancienne lors de l’opération. 
  
Vous pouvez modifier le remplacement des paramètres de comportement d’une forme de base de forme en modifiant le contrôleur de forme (dans la fenêtre **formes** , la forme avec le bouton droit, pointez sur **Modifier la forme**, puis cliquez sur **Modifier la forme de base**) et modification des valeurs de le [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)et [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) des cellules dans la feuille ShapeSheet de la forme de base. 
  
> [!NOTE]
> Vous ne pouvez pas modifier les comportements de remplacement de forme des formes qui sont inclus dans les gabarits intégrés dans Microsoft Visio 2013. Pour modifier les comportements de remplacement de forme des formes Visio intégrés, créez un nouveau gabarit et ajoutez la forme que vous souhaitez modifier pour le nouveau gabarit. 
  

