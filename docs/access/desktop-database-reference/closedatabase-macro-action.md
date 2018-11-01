---
title: FermerBaseDonnées, action de macro
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42ba5925c35081f612bd4a81b49f3c2b16cf61dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876637"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="2826e-102">FermerBaseDonnées, action de macro</span><span class="sxs-lookup"><span data-stu-id="2826e-102">CloseDatabase Macro Action</span></span>


<span data-ttu-id="2826e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2826e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2826e-104">Vous pouvez utiliser l'action **FermerBaseDonnées** pour fermer la base de données active.</span><span class="sxs-lookup"><span data-stu-id="2826e-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="2826e-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="2826e-105">Setting</span></span>

<span data-ttu-id="2826e-106">L'action **FermerBaseDonnées** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="2826e-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2826e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="2826e-107">Remarks</span></span>

  - <span data-ttu-id="2826e-108">Access n'exécute aucune action indiquée à la suite de l'action **FermerBaseDonnées** dans une macro.</span><span class="sxs-lookup"><span data-stu-id="2826e-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="2826e-109">Cette action a le même effet que l’onglet **fichier** , puis cliquez sur **Fermer de la base de données**.</span><span class="sxs-lookup"><span data-stu-id="2826e-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="2826e-110">Si la base de données contient des objets qui n'ont pas été enregistrés lorsque vous exécutez l'action **FermerBaseDonnées**, des boîtes de dialogue identiques à celles qui s'affichent lorsque vous cliquez sur **Fermer la base de données** apparaissent.</span><span class="sxs-lookup"><span data-stu-id="2826e-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="2826e-111">Pour exécuter l'action **FermerBaseDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CloseDatabase** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="2826e-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

