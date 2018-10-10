---
title: AnnulerModificationEnregistrement, action de macro
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fe474f9ba7250e3225bc73460c6d192800c861b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470613"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="11eb0-102">AnnulerModificationEnregistrement, action de macro</span><span class="sxs-lookup"><span data-stu-id="11eb0-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="11eb0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="11eb0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="11eb0-104">Vous pouvez utiliser l'action **AnnulerModificationEnregistrement** pour annuler les modifications appliquées à un enregistrement dans un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)** avant que les modifications soient validées.</span><span class="sxs-lookup"><span data-stu-id="11eb0-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <P><span data-ttu-id="11eb0-105">[!REMARQUE] L'action <STRONG>AnnulerModificationEnregistrement</STRONG> est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="11eb0-105">The <STRONG>CancelRecordChange</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="11eb0-106">Notes</span><span class="sxs-lookup"><span data-stu-id="11eb0-106">Remarks</span></span>

<span data-ttu-id="11eb0-107">Lorsque vous appelez l'action **AnnulerModificationEnregistrement**, le bloc de données **CréerEnregistrement** ou **ModifierEnregistrement** est quitté immédiatement.</span><span class="sxs-lookup"><span data-stu-id="11eb0-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

