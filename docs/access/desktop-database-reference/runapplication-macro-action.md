---
title: RunApplication, action de macro
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306838"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="b2024-102">RunApplication, action de macro</span><span class="sxs-lookup"><span data-stu-id="b2024-102">RunApplication macro action</span></span>

<span data-ttu-id="b2024-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2024-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Note de sécurité" alt="Security note" /><span data-ttu-id="b2024-105"><strong>Note de sécurité</strong></span><span class="sxs-lookup"><span data-stu-id="b2024-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2024-p101">Soyez prudent lors de l’exécution de fichiers ou de code exécutables dans les macros ou les applications. Les fichiers ou le code exécutables peuvent être utilisés pour effectuer des actions pouvant compromettre la sécurité de votre ordinateur et de vos données.</span><span class="sxs-lookup"><span data-stu-id="b2024-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b2024-p102">Vous pouvez utiliser l'action **ExécuterApplication** pour exécuter une application Microsoft Windows ou MS-DOS telle que Microsoft Office Excel, Microsoft Office Word ou Microsoft Office PowerPoint dans Microsoft Office Access. Vous pouvez, par exemple, souhaiter coller des données d'une feuille de calcul Excel dans votre base de données Access.</span><span class="sxs-lookup"><span data-stu-id="b2024-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="b2024-110">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="b2024-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b2024-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2024-111">Setting</span></span>

<span data-ttu-id="b2024-112">L’action **ExécuterApplication** utilise l’argument suivant :</span><span class="sxs-lookup"><span data-stu-id="b2024-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2024-113">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="b2024-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b2024-114">Description</span><span class="sxs-lookup"><span data-stu-id="b2024-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2024-115"><strong>Ligne de commande</strong></span><span class="sxs-lookup"><span data-stu-id="b2024-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="b2024-p103">Ligne de commande est utilisé pour démarrer l’application (y compris le chemin d’accès et tous les paramètres nécessaires, tels que les commutateurs qui exécutent l’application dans un mode particulier). Tapez la ligne de commande dans la zone <strong>Ligne commande</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b2024-p103">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2024-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2024-119">Remarks</span></span>

<span data-ttu-id="b2024-p104">L'application sélectionnée avec cette action est chargée et s'exécute en avant-plan. La macro comprenant cette action continue de s'exécuter après avoir démarré l'application.</span><span class="sxs-lookup"><span data-stu-id="b2024-p104">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="b2024-p105">Vous pouvez transférer les données entre l'autre application et Access à l'aide de la fonctionnalité d'échange dynamique de données (DDE) Microsoft Windows ou le Presse-papiers. Vous pouvez utiliser l'action **EnvoiTouches** pour envoyer une séquence de touches à l'autre application (bien que l'échange dynamique de données soit plus efficace pour le transfert de données). Vous pouvez également partager des données entre applications à l'aide de l'automation.</span><span class="sxs-lookup"><span data-stu-id="b2024-p105">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span></span>

<span data-ttu-id="b2024-125">Les applications MS-DOS sont exécutées dans une fenêtre MS-DOS au sein de l'environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="b2024-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="b2024-126">Dans les systèmes d'exploitation Windows, il existe plusieurs façons d'exécuter une application, notamment en démarrant le programme à partir de l'Explorateur Windows, en utilisant la commande **Exécuter** du menu **Démarrer** ou en double-cliquant sur l'icône d'un programme dans le Bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="b2024-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="b2024-p106">Vous ne pouvez pas exécuter l'action **ExécuterApplication** dans un module Visual Basic pour Applications (VBA). Utilisez à la place la fonction **Shell** VBA.</span><span class="sxs-lookup"><span data-stu-id="b2024-p106">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span></span>

