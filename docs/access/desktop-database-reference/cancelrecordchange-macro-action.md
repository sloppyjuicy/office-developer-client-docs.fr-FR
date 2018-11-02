---
title: CancelRecordChange, action de macro
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb414837696eecc028d864c1efa9f74251f596a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919331"
---
# <a name="cancelrecordchange-macro-action"></a>CancelRecordChange, action de macro


**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **AnnulerModificationEnregistrement** pour annuler les modifications appliquées à un enregistrement dans un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)** avant que les modifications soient validées.


> [!NOTE]
> [!REMARQUE] L'action **AnnulerModificationEnregistrement** est disponible uniquement dans les macros de données.



## <a name="remarks"></a>Notes

Lorsque vous appelez l'action **AnnulerModificationEnregistrement**, le bloc de données **CréerEnregistrement** ou **ModifierEnregistrement** est quitté immédiatement.

