---
title: CancelRecordChange Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Vous pouvez utiliser l'action AnnulerModificationEnregistrement pour annuler les modifications appliquées à un enregistrement dans un bloc de données CréerEnregistrement ou ModifierEnregistrement avant que les modifications soient validées.
ms.openlocfilehash: 3d0d814ccbde4f0506c593ed5b33dabb50c18dd3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370539"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a>CancelRecordChange Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l'action **AnnulerModificationEnregistrement** pour annuler les modifications appliquées à un enregistrement dans un bloc de données **[CréerEnregistrement](createrecord-data-block-access-custom-web-app.md)** ou **[ModifierEnregistrement](editrecord-data-block-access-custom-web-app.md)** avant que les modifications soient validées.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
> [!NOTE]
> L’action **AnnulerModificationEnregistrement** est disponible uniquement dans les macros de données.
  
## <a name="remarks"></a>Remarques

Lorsque vous appelez l'action **AnnulerModificationEnregistrement**, le bloc de données **CréerEnregistrement** ou **ModifierEnregistrement** est quitté immédiatement.
  