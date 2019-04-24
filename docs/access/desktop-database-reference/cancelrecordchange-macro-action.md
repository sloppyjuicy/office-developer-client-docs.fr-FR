---
title: CancelRecordChange, action de macro
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296653"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="47dc8-102">CancelRecordChange, action de macro</span><span class="sxs-lookup"><span data-stu-id="47dc8-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="47dc8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47dc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47dc8-104">Vous pouvez utiliser l'action **AnnulerModificationEnregistrement** pour annuler les modifications appliquées à un enregistrement dans un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)** avant que les modifications soient validées.</span><span class="sxs-lookup"><span data-stu-id="47dc8-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="47dc8-105">[!REMARQUE] L'action **AnnulerModificationEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="47dc8-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="47dc8-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="47dc8-106">Remarks</span></span>

<span data-ttu-id="47dc8-107">Lorsque vous appelez l'action **AnnulerModificationEnregistrement**, le bloc de données **CréerEnregistrement** ou **ModifierEnregistrement** est quitté immédiatement.</span><span class="sxs-lookup"><span data-stu-id="47dc8-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

