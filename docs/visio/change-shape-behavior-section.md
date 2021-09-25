---
title: Change Shape Behavior Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Détermine les propriétés transférées de l’ancienne forme vers la forme de remplacement lors d’une opération de remplacement. Les valeurs des cellules de la section Modifier le comportement de la forme de la forme de base du remplacement sont lues pendant l’opération de remplacement de la forme.
ms.openlocfilehash: 4bc87c7ab77568b06ced5456c74f96c151322761
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577996"
---
# <a name="change-shape-behavior-section"></a>Change Shape Behavior Section

Détermine les propriétés transférées de l’ancienne forme vers la forme de remplacement lors d’une opération de remplacement. Les valeurs des cellules de la section **Modifier** le comportement de la forme de la forme de base du remplacement sont lues pendant l’opération de remplacement de la forme. 
  
## <a name="remarks"></a>Remarques

En fixant les cellules de la section **Modifier** le comportement de la forme, vous pouvez vous assurer que certaines propriétés de la forme de remplacement restent inchangées pendant l’opération de remplacement. Les propriétés qui ne sont pas protégées sont mises à jour avec les valeurs de forme locales de l’ancienne forme pendant l’opération. 
  
Vous pouvez modifier les paramètres de comportement de remplacement d’une forme de base en modifiant la forme de base (dans la fenêtre **Formes,** cliquez avec le bouton droit sur la forme, pointez sur Modifier la forme de **base,** puis cliquez sur Modifier la forme de **base)** et en modifiant les valeurs des cellules [ReplaceCopyCells,](replacecopycells-cell-change-shape-behavior-section.md) [ReplaceLockFormat,](replacelockformat-cell-change-shape-behavior-section.md) [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)et [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) dans la feuille ShapeSheet de la forme de base. 
  
> [!NOTE]
> Vous ne pouvez pas modifier les comportements de remplacement des formes incluses dans les gabarits intégrés dans Microsoft Visio 2013. Pour modifier les comportements de remplacement de forme des formes Visio intégrées, créez un gabarit et ajoutez la forme que vous souhaitez modifier au nouveau gabarit. 
  

