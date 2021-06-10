---
title: Bip, action de macro (référence de base de données de bureau Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296863"
---
# <a name="beep-macro-action"></a><span data-ttu-id="009a3-102">Beep, action de macro</span><span class="sxs-lookup"><span data-stu-id="009a3-102">Beep macro action</span></span>


<span data-ttu-id="009a3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="009a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="009a3-104">Utilisez l’action **Bip** pour émettre un signal sonore dans les haut-parleurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="009a3-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="009a3-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="009a3-105">Setting</span></span>

<span data-ttu-id="009a3-106">L’action **Bip** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="009a3-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="009a3-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="009a3-107">Remarks</span></span>

<span data-ttu-id="009a3-108">Vous pouvez utiliser l’action **Bip** pour signaler les occurrences suivantes :</span><span class="sxs-lookup"><span data-stu-id="009a3-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="009a3-109">des modifications importantes ont été apportées à l'écran ;</span><span class="sxs-lookup"><span data-stu-id="009a3-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="009a3-p101">le type de données entré dans un contrôle est incorrect. Par exemple, l'utilisateur a entré des donnes numériques dans un contrôle zone de texte ;</span><span class="sxs-lookup"><span data-stu-id="009a3-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="009a3-112">une macro a atteint un point spécifique ou a terminé ses actions.</span><span class="sxs-lookup"><span data-stu-id="009a3-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="009a3-113">La fréquence et la durée du signal sonore dépendent du matériel, qui peut varier d'un ordinateur à un autre.</span><span class="sxs-lookup"><span data-stu-id="009a3-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="009a3-114">Pour exécuter l'action **Bip** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Beep** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="009a3-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

